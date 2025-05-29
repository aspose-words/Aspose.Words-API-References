---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words لـ .NET
description: تأكد من جودة مستندك باستخدام خاصية التدقيق النحوي. تأكد من صحة نصك ودقته للحصول على نتائج احترافية ومنقحة.
type: docs
weight: 190
url: /ar/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

إرجاع`حقيقي` إذا تم التحقق من القواعد النحوية للمستند.

```csharp
public bool GrammarChecked { get; set; }
```

## ملاحظات

لإعادة التحقق من القواعد النحوية في المستند، اضبط هذه الخاصية على`خطأ شنيع` .

## أمثلة

يوضح كيفية ضبط التحقق من الإملاء أو القواعد النحوية.

```csharp
Document doc = new Document();

// السلسلة التي تحتوي على أخطاء إملائية.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// تبدأ عملية التدقيق الإملائي/النحوي إذا قمنا بتعيين الخصائص على خطأ.
// يمكننا رؤية جميع الأخطاء في Microsoft Word عبر المراجعة -> التدقيق الإملائي والنحوي.
// لاحظ أن Microsoft Word لا يبدأ فحص القواعد النحوية/الإملائية تلقائيًا لتنسيقات المستندات DOC وRTF.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
