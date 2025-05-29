---
title: Footnote.FootnoteType
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية FootnoteType، وتعرف بسهولة على الحواشي السفلية أو النهائية في مستنداتك لتحسين الوضوح والتنظيم.
type: docs
weight: 30
url: /ar/net/aspose.words.notes/footnote/footnotetype/
---
## Footnote.FootnoteType property

ترجع قيمة تحدد ما إذا كانت هذه حاشية سفلية أم حاشية ختامية.

```csharp
public FootnoteType FootnoteType { get; }
```

## أمثلة

يظهر الفرق بين الحواشي السفلية والحواشي النهائية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// فيما يلي طريقتان لإضافة مراجع مرقمة إلى النص. سيضيف كلا المرجعين
// علامة مرجعية صغيرة علوية في المكان الذي نقوم بإدخالها فيه.
// علامة المرجع، بشكل افتراضي، هي رقم فهرس المرجع بين جميع المراجع في المستند.
// سيؤدي كل مرجع أيضًا إلى إنشاء إدخال، والذي سيكون له نفس علامة المرجع الموجودة في نص الموضوع
// والنص المرجعي، الذي سنمرره إلى طريقة "InsertFootnote" الخاصة بمنشئ المستندات.
// 1 - حاشية سفلية، والتي ستظهر مدخلاتها في نفس الصفحة التي يوجد بها النص الذي تشير إليه:
builder.Write("Footnote referenced main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, 
    "Footnote text, will appear at the bottom of the page that contains the referenced text.");

// 2 - حاشية ختامية، والتي سيظهر إدخالها في نهاية المستند:
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
* مساحة الاسم [Aspose.Words.Notes](../../../aspose.words.notes/)
* المجسم [Aspose.Words](../../../)
