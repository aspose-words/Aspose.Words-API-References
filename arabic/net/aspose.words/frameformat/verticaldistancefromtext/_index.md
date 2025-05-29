---
title: FrameFormat.VerticalDistanceFromText
linktitle: VerticalDistanceFromText
articleTitle: VerticalDistanceFromText
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FrameFormat VerticalDistanceFromText لضبط المسافة الرأسية بسهولة في النقاط بين إطارك والنص المحيط به لتحسين التحكم في التخطيط.
type: docs
weight: 100
url: /ar/net/aspose.words/frameformat/verticaldistancefromtext/
---
## FrameFormat.VerticalDistanceFromText property

يحدد المسافة الرأسية (بالنقاط) بين الإطار والنص المحيط به.

```csharp
public double VerticalDistanceFromText { get; }
```

## أمثلة

يوضح كيفية الحصول على معلومات حول خصائص تنسيق الفقرات التي تعتبر إطارات.

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

* class [FrameFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
