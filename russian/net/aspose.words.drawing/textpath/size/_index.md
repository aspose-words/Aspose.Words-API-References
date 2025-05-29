---
title: TextPath.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextPath Size, легко настройте размер шрифта в пунктах для улучшения читабельности и гибкости дизайна в ваших проектах.
type: docs
weight: 120
url: /ru/net/aspose.words.drawing/textpath/size/
---
## TextPath.Size property

Определяет размер шрифта в пунктах.

```csharp
public double Size { get; set; }
```

## Примечания

Значение по умолчанию — 36.

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

    // Применяем к тексту параметры форматирования «Жирный» и «Курсив», используя соответствующие свойства.
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

    // Используйте свойство «On», чтобы показать/скрыть текст.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Используйте свойство «Кернинг» для включения/отключения интервала кернинга между определенными символами.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Используйте свойство «Интервал», чтобы задать пользовательский интервал между символами по шкале от 0,0 (нет) до 1,0 (по умолчанию).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Установите свойство «RotateLetters» в значение «true», чтобы повернуть каждый символ на 90 градусов против часовой стрелки.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Установите свойство «SameLetterHeights» в значение «true», чтобы x-высота каждого символа была равна высоте заглавной буквы.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // По умолчанию размер текста всегда будет масштабироваться в соответствии с размером содержащей его фигуры, переопределяя настройку размера текста.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Если мы установим свойство "FitShape:" на "false", текст сохранит размер
    // который свойство «Размер» определяет независимо от размера фигуры.
    // Используйте свойство "TextPathAlignment" также для выравнивания текста по стороне фигуры.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// Вставьте новый абзац с фигурой WordArt внутри.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Создаем встроенную фигуру, которая будет служить контейнером для нашего WordArt.
    // Фигура может быть допустимой фигурой WordArt только в том случае, если мы назначаем ей ShapeType, обозначенный в WordArt.
    // Эти типы будут иметь в описании «объект WordArt»,
    // и имена их констант перечислителя будут начинаться с «Text».
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
