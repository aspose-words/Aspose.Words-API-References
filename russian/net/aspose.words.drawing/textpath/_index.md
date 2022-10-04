---
title: TextPath
second_title: Справочник по API Aspose.Words для .NET
description: Определяет текст и форматирование пути к тексту объекта WordArt.
type: docs
weight: 1200
url: /ru/net/aspose.words.drawing/textpath/
---
## TextPath class

Определяет текст и форматирование пути к тексту (объекта WordArt).

```csharp
public class TextPath
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | Истинно, если шрифт отформатирован как полужирный. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Определяет, соответствует ли текст контуру фигуры. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Определяет, соответствует ли текст ограничивающей рамке фигуры. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Определяет семейство шрифтов textpath. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | Истинно, если шрифт отформатирован как курсив. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Определяет, включен ли кернинг. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Определяет, будет ли отображаться текст. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Определяет, является ли порядок расположения строк обратным. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Определяет, повернуты ли буквы текста. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Определяет, будут ли все буквы одинаковой высоты независимо от начального регистра. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Определяет, применяется ли тень к тексту на текстовом пути. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Определяет размер шрифта в пунктах. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | Истинно, если шрифт отформатирован как маленькие заглавные буквы. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Определяет расстояние между текстом. 1 означает 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | Истинно, если шрифт отформатирован как зачеркнутый текст. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Определяет текст текстового пути. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Определяет выравнивание текста. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Определяет, удаляется ли лишнее пространство над и под текстом. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | Истинно, если шрифт подчеркнут. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Определяет, будет ли использоваться прямой текстовый путь вместо контура формы. |

### Примечания

Использовать[`TextPath`](../shape/textpath/) для доступа к свойствам WordArt фигуры. Вы не создаете экземпляры[`TextPath`](./textpath/) класс напрямую.

### Примеры

Показывает, как работать с WordArt.

```csharp
{
    Document doc = new Document();

    // Вставьте объект WordArt, чтобы отобразить текст в форме, размер которой можно изменять и перемещать с помощью мыши в Microsoft Word.
    // Укажите "ShapeType" в качестве аргумента, чтобы установить форму для WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // Применяем к тексту настройки форматирования "Жирный" и "Курсив" с помощью соответствующих свойств.
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

    // Используйте свойство «Вкл.», чтобы показать/скрыть текст.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // Используйте свойство «Кернинг», чтобы включить/отключить интервал кернинга между определенными символами.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // Используйте свойство «Интервал», чтобы установить пользовательский интервал между символами по шкале от 0,0 (нет) до 1,0 (по умолчанию).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // Установите для свойства "RotateLetters" значение "true", чтобы повернуть каждый символ на 90 градусов против часовой стрелки.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // Установите для свойства «SameLetterHeights» значение «true», чтобы получить высоту x каждого символа, равную высоте прописной буквы.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // По умолчанию размер текста всегда будет масштабироваться в соответствии с размером содержащей его фигуры, переопределяя настройку размера текста.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // Если мы установим для свойства "FitShape:" значение "false", текст сохранит размер
    // который указывает свойство "Размер" независимо от размера фигуры.
    // Используйте свойство "TextPathAlignment" также для выравнивания текста по стороне фигуры.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");

/// <summary>
/// Вставьте новый абзац с фигурой WordArt внутри него.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // Создайте встроенную фигуру, которая будет служить контейнером для нашего WordArt.
    // Фигура может быть допустимой фигурой WordArt только в том случае, если мы назначаем ей ShapeType, назначенный WordArt.
    // Эти типы будут иметь в описании "объект WordArt",
    // и все их имена констант перечислителя будут начинаться с "Text".
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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
