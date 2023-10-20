---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.TextPath сорт. Определяет текст и форматирование текстового пути объекта WordArt на С#.
type: docs
weight: 1350
url: /ru/net/aspose.words.drawing/textpath/
---
## TextPath class

Определяет текст и форматирование текстового пути (объекта WordArt).

Чтобы узнать больше, посетите[Работа с фигурами](https://docs.aspose.com/words/net/working-with-shapes/) статья документации.

```csharp
public class TextPath
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | True, если шрифт отформатирован как жирный. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | Определяет, соответствует ли текст контуру фигуры. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | Определяет, помещается ли текст в ограничивающую рамку фигуры. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | Определяет семейство шрифта текстового пути. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | True, если шрифт отформатирован как курсив. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | Определяет, включен ли кернинг. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | Определяет, отображается ли текст. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | Определяет, обратный ли порядок расположения строк. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | Определяет, поворачиваются ли буквы текста. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | Определяет, будут ли все буквы одинаковой высоты независимо от начального регистра. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | Определяет, применяется ли тень к тексту на пути к тексту. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | Определяет размер шрифта в пунктах. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | True, если шрифт отформатирован как маленькие заглавные буквы. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | Определяет расстояние для текста. 1 означает 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | True, если шрифт отформатирован как зачеркнутый текст. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | Определяет текст текстового пути. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | Определяет выравнивание текста. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | Определяет, удаляется ли лишнее пространство выше и ниже текста. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | True, если шрифт подчеркнут. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | Определяет, будет ли использоваться прямой текстовый путь вместо контура фигуры. |

## Примечания

Использовать[`TextPath`](../shape/textpath/) для доступа к свойствам фигуры WordArt. Вы не создаете экземпляры`TextPath` класс напрямую.

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

* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
