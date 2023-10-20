---
title: TextPath.Italic
linktitle: Italic
articleTitle: Italic
second_title: Aspose.Words для .NET
description: TextPath Italic свойство. True если шрифт отформатирован как курсив на С#.
type: docs
weight: 50
url: /ru/net/aspose.words.drawing/textpath/italic/
---
## TextPath.Italic property

True, если шрифт отформатирован как курсив.

```csharp
public bool Italic { get; set; }
```

## Примечания

Значение по умолчанию:`ЛОЖЬ`.

## Примеры

Показывает, как работать с WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // Вставьте объект WordArt для отображения текста в форме, размер которой можно изменять и перемещать с помощью мыши в Microsoft Word.
    // Укажите «ShapeType» в качестве аргумента, чтобы задать форму для WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Примените к тексту параметры форматирования «Жирный» и «Курсив», используя соответствующие свойства.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // Ниже приведены различные другие свойства, связанные с форматированием текста.
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    // Используйте свойство «Вкл», чтобы показать/скрыть текст.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Используйте свойство «Кернинг», чтобы включить/отключить интервал кернинга между определенными символами.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Используйте свойство «Интервал», чтобы установить собственный интервал между символами по шкале от 0,0 (нет) до 1,0 (по умолчанию).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Установите для свойства RotateLetters значение true, чтобы повернуть каждый символ на 90 градусов против часовой стрелки.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Установите для свойства SameLetterHeights значение «true», чтобы высота x каждого символа была равна высоте верхнего предела.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // По умолчанию размер текста всегда масштабируется в соответствии с размером содержащейся фигуры, переопределяя настройку размера текста.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Если мы установим для свойства FitShape: значение «false», текст сохранит размер
    // которое задает свойство "Размер" независимо от размера фигуры.
    // Используйте свойство TextPathAlignment также для выравнивания текста по сторонам фигуры.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Вставьте новый абзац с фигурой WordArt внутри него.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Создаем встроенную фигуру, которая будет служить контейнером для нашего WordArt.
    // Фигура может быть допустимой фигурой WordArt только в том случае, если мы присвоим ей ShapeType, назначенный WordArt.
    // Эти типы будут иметь в описании «объект WordArt»,
    // и имена констант их перечислителей будут начинаться с «Текст».
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### Смотрите также

* class [TextPath](../)
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
