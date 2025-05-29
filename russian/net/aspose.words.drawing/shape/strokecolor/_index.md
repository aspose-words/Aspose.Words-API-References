---
title: Shape.StrokeColor
linktitle: StrokeColor
articleTitle: StrokeColor
second_title: Aspose.Words для .NET
description: Настройте свой дизайн с помощью свойства Shape StrokeColor, позволяющего определять яркие цвета обводки для создания потрясающего визуального эффекта.
type: docs
weight: 200
url: /ru/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

Определяет цвет обводки.

```csharp
public Color StrokeColor { get; set; }
```

## Примечания

Это ярлык для[`Color`](../../stroke/color/) свойство.

Значение по умолчанию: Black .

## Примеры

Показывает, как залить фигуру сплошным цветом.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Напишите текст, а затем закройте его плавающей фигурой.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// Используйте свойство "StrokeColor", чтобы задать цвет контура фигуры.
shape.StrokeColor = Color.CadetBlue;

// Используйте свойство «FillColor», чтобы задать цвет внутренней области фигуры.
shape.FillColor = Color.LightBlue;

// Свойство «Непрозрачность» определяет прозрачность цвета по шкале от 0 до 1,
// где 1 — полностью непрозрачный, а 0 — невидимый.
// Заливка фигуры по умолчанию полностью непрозрачна, поэтому мы не можем видеть текст, над которым находится эта фигура.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// Установите меньшее значение непрозрачности цвета заливки фигуры, чтобы мы могли видеть текст под ней.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

Показывает, как перебрать все фигуры в документе.

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Регистрирует информацию, связанную с внешним видом посещенных фигур.
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
    /// Добавляет строку в StringBuilder с одним добавленным символом табуляции для каждого уровня отступа.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Возвращаем весь текст, накопленный StringBuilder.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Вызывается, когда посетитель посещает начало узла Shape.
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
    /// Вызывается, когда посетитель посещает конец узла Shape.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда посетитель посещает начало узла GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Вызывается, когда посетитель посещает конец узла GroupShape.
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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
