---
title: FrameFormat Class
linktitle: FrameFormat
articleTitle: FrameFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.FrameFormat لتنسيق الإطارات المتقدم في الفقرات. حسّن تصميم مستندك بتكامل سلس ومرونته.
type: docs
weight: 3500
url: /ar/net/aspose.words/frameformat/
---
## FrameFormat class

يمثل التنسيق المرتبط بالإطار للفقرة.

```csharp
public class FrameFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Height](../../aspose.words/frameformat/height/) { get; } | يحصل على ارتفاع الإطار المحدد. |
| [HeightRule](../../aspose.words/frameformat/heightrule/) { get; } | يحصل على القاعدة لتحديد ارتفاع الإطار المحدد. |
| [HorizontalAlignment](../../aspose.words/frameformat/horizontalalignment/) { get; } | يحصل على محاذاة أفقية للإطار المحدد. |
| [HorizontalDistanceFromText](../../aspose.words/frameformat/horizontaldistancefromtext/) { get; } | يحصل على المسافة الأفقية بين الإطار والنص المحيط به، بالنقاط. |
| [HorizontalPosition](../../aspose.words/frameformat/horizontalposition/) { get; } | يحصل على المسافة الأفقية بين حافة الإطار والعنصر المحدد بواسطة[`RelativeHorizontalPosition`](./relativehorizontalposition/) الملكية. |
| [IsFrame](../../aspose.words/frameformat/isframe/) { get; } | إرجاع`حقيقي` إذا كانت الفقرة عبارة عن إطار. |
| [RelativeHorizontalPosition](../../aspose.words/frameformat/relativehorizontalposition/) { get; } | يحصل على الموضع الأفقي النسبي للإطار. |
| [RelativeVerticalPosition](../../aspose.words/frameformat/relativeverticalposition/) { get; } | يحصل على الموضع الرأسي النسبي للإطار. |
| [VerticalAlignment](../../aspose.words/frameformat/verticalalignment/) { get; } | يحصل على محاذاة رأسية للإطار المحدد. |
| [VerticalDistanceFromText](../../aspose.words/frameformat/verticaldistancefromtext/) { get; } | يحدد المسافة الرأسية (بالنقاط) بين الإطار والنص المحيط به. |
| [VerticalPosition](../../aspose.words/frameformat/verticalposition/) { get; } | يحصل على المسافة الرأسية بين حافة الإطار والعنصر المحدد بواسطة[`RelativeVerticalPosition`](./relativeverticalposition/) الملكية. |
| [Width](../../aspose.words/frameformat/width/) { get; } | يحصل على عرض الإطار المحدد، بالنقاط. |

## ملاحظات

يتم إنشاء هذا الكائن دائمًا. إذا كانت الفقرة إطارًا، فستحتوي جميع الخصائص على قيم مناسبة، وإلا، فسيتم تعيين جميع الخصائص على قيمها الافتراضية.

يستخدم[`IsFrame`](./isframe/)للتحقق مما إذا كانت الفقرة عبارة عن إطار.

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

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
