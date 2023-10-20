---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.FrameFormat فصل. يمثل التنسيق المتعلق بالإطار للفقرة في C#.
type: docs
weight: 3070
url: /ar/net/aspose.words/frameformat/
---
## FrameFormat class

يمثل التنسيق المتعلق بالإطار للفقرة.

```csharp
public class FrameFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | الحصول على ارتفاع الإطار المحدد. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | الحصول على قاعدة تحديد ارتفاع الإطار المحدد. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | الحصول على المحاذاة الأفقية للإطار المحدد. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | يحصل على المسافة الأفقية بين الإطار والنص المحيط بالنقاط. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | يحصل على المسافة الأفقية بين حافة الإطار والعنصر المحدد بواسطة[`RelativeHorizontalPosition`](./relativehorizontalposition/) الملكية. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | إرجاع`حقيقي` إذا كانت الفقرة عبارة عن إطار. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | يحصل على الموضع الأفقي النسبي للإطار. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | يحصل على الموضع الرأسي النسبي للإطار. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | الحصول على المحاذاة الرأسية للإطار المحدد. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | يحدد المسافة الرأسية (بالنقاط) بين الإطار والنص المحيط. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | يحصل على المسافة العمودية بين حافة الإطار والعنصر المحدد بواسطة[`RelativeVerticalPosition`](./relativeverticalposition/) الملكية. |
| [Width](../../aspose.words/frameformat/width/) { get; } | الحصول على عرض الإطار المحدد بالنقاط. |

## ملاحظات

يتم إنشاء هذا الكائن دائمًا. إذا كانت الفقرة عبارة عن إطار، فستحتوي جميع الخصائص على قيم خاصة بها، وإلا فسيتم تعيين جميع الخصائص إلى إعداداتها الافتراضية.

يستخدم[`IsFrame`](./isframe/) للتحقق مما إذا كانت الفقرة عبارة عن إطار.

## أمثلة

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
