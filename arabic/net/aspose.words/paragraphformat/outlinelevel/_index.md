---
title: ParagraphFormat.OutlineLevel
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. يحدد مستوى المخطط التفصيلي للفقرة في المستند.
type: docs
weight: 250
url: /ar/net/aspose.words/paragraphformat/outlinelevel/
---
## ParagraphFormat.OutlineLevel property

يحدد مستوى المخطط التفصيلي للفقرة في المستند.

```csharp
public OutlineLevel OutlineLevel { get; set; }
```

### أمثلة

يوضح كيفية تكوين مستويات المخطط التفصيلي للفقرة لإنشاء نص قابل للطي.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// تحتوي كل فقرة على OutlineLevel، والذي يمكن أن يكون أي رقم من 1 إلى 9، أو بالقيمة الافتراضية "BodyText".
// سيؤدي تعيين الخاصية إلى إحدى القيم المرقمة إلى ظهور سهم إلى اليسار
// بداية الفقرة.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level1;
builder.Writeln("Paragraph outline level 1.");

// المستوى 1 هو المستوى الأعلى. إذا كانت هناك فقرة ذات مستوى أدنى أسفل فقرة ذات مستوى أعلى،
// سيؤدي طي الفقرة ذات المستوى الأعلى إلى طي الفقرة ذات المستوى الأدنى.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level2;
builder.Writeln("Paragraph outline level 2.");

// فقرتان من نفس المستوى لن تنهارا،
// ولا تؤدي الأسهم إلى طي الفقرات التي تشير إليها.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.Level3;
builder.Writeln("Paragraph outline level 3.");
builder.Writeln("Paragraph outline level 3.");

// قيمة "BodyText" الافتراضية هي الأدنى، والتي يمكن طيها لفقرة من أي مستوى.
builder.ParagraphFormat.OutlineLevel = OutlineLevel.BodyText;
builder.Writeln("Paragraph at main text level.");

doc.Save(ArtifactsDir + "ParagraphFormat.ParagraphOutlineLevel.docx");
```

### أنظر أيضا

* enum [OutlineLevel](../../outlinelevel/)
* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


