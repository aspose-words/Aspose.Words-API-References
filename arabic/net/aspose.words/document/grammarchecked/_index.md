---
title: Document.GrammarChecked
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. إرجاعحقيقي إذا تم تدقيق المستند من الناحية النحوية.
type: docs
weight: 180
url: /ar/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

إرجاع`حقيقي` إذا تم تدقيق المستند من الناحية النحوية.

```csharp
public bool GrammarChecked { get; set; }
```

### ملاحظات

لإعادة التدقيق النحوي في المستند، قم بتعيين هذه الخاصية إلى`خطأ شنيع` .

### أمثلة

يوضح كيفية تعيين التدقيق الإملائي أو النحوي.

```csharp
Document doc = new Document();

// السلسلة التي بها أخطاء إملائية.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // يبدأ التدقيق الإملائي/النحوي إذا قمنا بتعيين الخصائص على خطأ.
// يمكننا رؤية جميع الأخطاء في Microsoft Word عبر المراجعة -> التهجئة & قواعد.
// لاحظ أن Microsoft Word لا يبدأ التدقيق النحوي/الإملائي تلقائيًا لتنسيق مستند DOC وRTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


