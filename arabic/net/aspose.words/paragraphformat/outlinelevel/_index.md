---
title: ParagraphFormat.OutlineLevel
linktitle: OutlineLevel
articleTitle: OutlineLevel
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat OutlineLevel لتحديد التسلسل الهرمي للفقرات في مستنداتك بسهولة، مما يعزز التنظيم وسهولة القراءة.
type: docs
weight: 260
url: /ar/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

يحدد مستوى المخطط التفصيلي للفقرة في المستند.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

## أمثلة

يوضح كيفية تكوين مستويات مخطط الفقرة لإنشاء نص قابل للطي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحتوي كل فقرة على OutlineLevel، والذي يمكن أن يكون أي رقم من 1 إلى 9، أو قيمة "BodyText" الافتراضية.
// سيؤدي تعيين الخاصية إلى إحدى القيم المرقمة إلى إظهار سهم إلى اليسار
// من بداية الفقرة.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// المستوى ١ هو المستوى الأعلى. إذا كانت هناك فقرة ذات مستوى أدنى أسفل فقرة ذات مستوى أعلى،
// سيؤدي انهيار الفقرة ذات المستوى الأعلى إلى انهيار الفقرة ذات المستوى الأدنى.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// لن تنهار فقرتان من نفس المستوى مع بعضهما البعض،
// والسهام لا تنهار الفقرات التي تشير إليها.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// القيمة الافتراضية لـ "BodyText" هي الأدنى، والتي يمكن لفقرة من أي مستوى أن تنهار عندها.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### أنظر أيضا

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
