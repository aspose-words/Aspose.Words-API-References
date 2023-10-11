---
title: Footnote.FootnoteType
second_title: Aspose.Words لمراجع .NET API
description: Footnote ملكية. تُرجع قيمة تحدد ما إذا كانت هذه حاشية سفلية أم تعليق ختامي.
type: docs
weight: 20
url: /ar/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

تُرجع قيمة تحدد ما إذا كانت هذه حاشية سفلية أم تعليق ختامي.

```csharp
public FootnoteType FootnoteType { get; }
```

### أمثلة

يوضح الفرق بين الحواشي السفلية والتعليقات الختامية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لإرفاق مراجع مرقمة بالنص. سيضيف كلا هذين المرجعين أ
// علامة مرجعية صغيرة مرتفعة في الموقع الذي نقوم بإدراجها فيه.
// العلامة المرجعية، بشكل افتراضي، هي رقم فهرس المرجع بين جميع المراجع في المستند.
// سيقوم كل مرجع أيضًا بإنشاء إدخال، والذي سيكون له نفس العلامة المرجعية الموجودة في النص الأساسي
// والنص المرجعي، الذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
// 1 - حاشية سفلية، ستظهر مُدخلتها في نفس الصفحة التي يوجد بها النص الذي تشير إليه:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - حاشية ختامية تظهر مدخلاتها في نهاية المستند:
builder.Write("Endnote referenced main body text.");
Footnote endnote = builder.InsertFootnote(FootnoteType.Endnote, 
    "Endnote text, will appear at the very end of the document.");

builder.InsertBreak(BreakType.SectionBreakNewPage);
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(FootnoteType.Footnote, footnote.FootnoteType);
Assert.AreEqual(FootnoteType.Endnote, endnote.FootnoteType);

doc.Save(ArtifactsDir + "InlineStory.FootnoteEndnote.docx");
```

### أنظر أيضا

* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* مساحة الاسم [Aspose.Words.Notes](../../footnote/)
* المجسم [Aspose.Words](../../../)


