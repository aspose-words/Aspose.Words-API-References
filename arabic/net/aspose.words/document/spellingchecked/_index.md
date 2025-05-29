---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words لـ .NET
description: تأكد من خلو مستندك من الأخطاء الإملائية باستخدام خاصية التدقيق الإملائي. تأكد من أن محتواك قد خضع لتدقيق إملائي دقيق لضمان الاحترافية.
type: docs
weight: 430
url: /ar/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

إرجاع`حقيقي` إذا تم التحقق من صحة التهجئة في المستند.

```csharp
public bool SpellingChecked { get; set; }
```

## ملاحظات

لإعادة التحقق من التهجئة في المستند، اضبط هذه الخاصية على`خطأ شنيع` .

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
