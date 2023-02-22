---
title: Class FrameFormat
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.FrameFormat сорт. Представляет форматирование абзаца связанное с фреймом.
type: docs
weight: 2890
url: /ru/net/aspose.words/frameformat/
---
## FrameFormat class

Представляет форматирование абзаца, связанное с фреймом.

```csharp
public class FrameFormat
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | Получает высоту указанного кадра. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | Получает правило определения высоты указанного кадра. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | Получает горизонтальное выравнивание указанного кадра. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | Получает горизонтальное расстояние между фреймом и окружающим текстом в пунктах. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | Получает расстояние по горизонтали между краем кадра и элементом, указанным[`RelativeHorizontalPosition`](./relativehorizontalposition/) свойство. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | Возвращает true, если абзац является фреймом. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | Получает относительное положение кадра по горизонтали. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | Получает относительное вертикальное положение кадра. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | Получает вертикальное выравнивание указанного кадра. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | Определяет расстояние по вертикали (в пунктах) между фреймом и окружающим текстом. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | Получает расстояние по вертикали между краем кадра и элементом, указанным[`RelativeVerticalPosition`](./relativeverticalposition/) свойство. |
| [Width](../../aspose.words/frameformat/width/) { get; } | Получает ширину указанного кадра в пунктах. |

### Примечания

Этот объект создается всегда. Если абзац является фреймом, то все свойства будут содержать соответствующие значения, в противном случае все свойства будут установлены по умолчанию.

Использовать[`IsFrame`](./isframe/) чтобы проверить, является ли абзац фреймом.

### Примеры

Показывает, как получить информацию о свойствах форматирования абзацев, являющихся фреймами.

```csharp
Document doc = new Document(MyDir + "Paragraph frame.docx");

Paragraph paragraphFrame = doc.FirstSection.Body.Paragraphs.OfType<Paragraph>().First(p => p.FrameFormat.IsFrame);

Assert.AreEqual(233.3d, paragraphFrame.FrameFormat.Width);
Assert.AreEqual(138.8d, paragraphFrame.FrameFormat.Height);
Assert.AreEqual(HeightRule.AtLeast, paragraphFrame.FrameFormat.HeightRule);
Assert.AreEqual(HorizontalAlignment.Default, paragraphFrame.FrameFormat.HorizontalAlignment);
Assert.AreEqual(VerticalAlignment.Default, paragraphFrame.FrameFormat.VerticalAlignment);
Assert.AreEqual(34.05d, paragraphFrame.FrameFormat.HorizontalPosition);
Assert.AreEqual(RelativeHorizontalPosition.Page, paragraphFrame.FrameFormat.RelativeHorizontalPosition);
Assert.AreEqual(9.0d, paragraphFrame.FrameFormat.HorizontalDistanceFromText);
Assert.AreEqual(20.5d, paragraphFrame.FrameFormat.VerticalPosition);
Assert.AreEqual(RelativeVerticalPosition.Paragraph, paragraphFrame.FrameFormat.RelativeVerticalPosition);
Assert.AreEqual(0.0d, paragraphFrame.FrameFormat.VerticalDistanceFromText);
```

### Смотрите также

* пространство имен [Aspose.Words](../../aspose.words/)
* сборка [Aspose.Words](../../)


