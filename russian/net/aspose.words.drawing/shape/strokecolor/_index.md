---
title: Shape.StrokeColor
second_title: Справочник по API Aspose.Words для .NET
description: Shape свойство. Определяет цвет обводки.
type: docs
weight: 190
url: /ru/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Определяет цвет обводки.

```csharp
public Color StrokeColor { get; set; }
```

### Примечания

Это ярлык для[`Color`](../../stroke/color/) имущество.

Значение по умолчанию: Black.

### Примеры

Показывает, как заполнить фигуру сплошным цветом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Напишите какой-нибудь текст, а затем накройте его плавающей фигурой.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Используйте свойство "StrokeColor", чтобы установить цвет контура фигуры.
shape.StrokeColor = Color.CadetBlue;

// Используйте свойство "FillColor", чтобы задать цвет внутренней области фигуры.
shape.FillColor = Color.LightBlue;

// Свойство "Непрозрачность" определяет, насколько прозрачен цвет по шкале от 0 до 1,
// где 1 полностью непрозрачно, а 0 невидимо.
// Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не можем видеть текст, поверх которого находится эта фигура.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Установите непрозрачность цвета заливки фигуры на более низкое значение, чтобы мы могли видеть текст под ним.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

Показывает, как перебирать все фигуры в документе.

```csharp
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Регистрирует связанную с внешним видом информацию о посещенных фигурах.
/// </summary>
private class ShapeAppearancePrinter : DocumentVisitor
{
    public ShapeAppearancePrinter()
    {
        mShapesVisited = 0;
        mTextIndentLevel = 0;
        mStringBuilder = new StringBuilder();
    }

    /// <summary>
    /// Добавляет строку в StringBuilder с одним предшествующим символом табуляции для каждого уровня отступа.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Вернуть весь текст, который накопил StringBuilder.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Вызывается, когда этот посетитель посещает начало узла Shape.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        AppendLine($"Shape found: {shape.ShapeType}");

        mTextIndentLevel++;

        if (shape.HasChart)
            AppendLine($"Has chart: {shape.Chart.Title.Text}");

        AppendLine($"Extrusion enabled: {shape.ExtrusionEnabled}");
        AppendLine($"Shadow enabled: {shape.ShadowEnabled}");
        AppendLine($"StoryType: {shape.StoryType}");

        if (shape.Stroked)
        {
            Assert.AreEqual(shape.Stroke.Color, shape.StrokeColor);
            AppendLine($"Stroke colors: {shape.Stroke.Color}, {shape.Stroke.Color2}");
            AppendLine($"Stroke weight: {shape.StrokeWeight}");

        }

        if (shape.Filled)
            AppendLine($"Filled: {shape.FillColor}");

        if (shape.OleFormat != null)
            AppendLine($"Ole found of type: {shape.OleFormat.ProgId}");

        if (shape.SignatureLine != null)
            AppendLine($"Found signature line for: {shape.SignatureLine.Signer}, {shape.SignatureLine.SignerTitle}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда этот посетитель посещает конец узла Shape.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда этот посетитель посещает начало узла GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда этот посетитель посещает конец узла GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mTextIndentLevel--;
        AppendLine($"End of {groupShape.ShapeType}");

        return VisitorAction.Continue;
    }

    private int mShapesVisited;
    private int mTextIndentLevel;
    private readonly StringBuilder mStringBuilder;
}
```

### Смотрите также

* class [Shape](../)
* пространство имен [Aspose.Words.Drawing](../../shape/)
* сборка [Aspose.Words](../../../)


