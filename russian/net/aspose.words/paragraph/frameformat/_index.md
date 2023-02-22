---
title: Paragraph.FrameFormat
second_title: Справочник по API Aspose.Words для .NET
description: Paragraph свойство. Предоставляет доступ к свойствам форматирования абзаца.
type: docs
weight: 30
url: /ru/net/aspose.words/paragraph/frameformat/
---
## Paragraph.FrameFormat property

Предоставляет доступ к свойствам форматирования абзаца.

```csharp
public FrameFormat FrameFormat { get; }
```

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

* class [FrameFormat](../../frameformat/)
* class [Paragraph](../)
* пространство имен [Aspose.Words](../../paragraph/)
* сборка [Aspose.Words](../../../)


