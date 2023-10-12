---
title: FrameFormat.RelativeHorizontalPosition
second_title: Aspose.Words لمراجع .NET API
description: FrameFormat ملكية. يحصل على الموضع الأفقي النسبي للإطار.
type: docs
weight: 70
url: /ar/net/aspose.words/frameformat/relativehorizontalposition/
---
## FrameFormat.RelativeHorizontalPosition property

يحصل على الموضع الأفقي النسبي للإطار.

```csharp
public RelativeHorizontalPosition RelativeHorizontalPosition { get; }
```

### أمثلة

يوضح كيفية الحصول على معلومات حول خصائص تنسيق الفقرات التي تكون إطارات.

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

### أنظر أيضا

* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* class [FrameFormat](../)
* مساحة الاسم [Aspose.Words](../../frameformat/)
* المجسم [Aspose.Words](../../../)


