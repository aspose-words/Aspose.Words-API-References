---
title: Document.ShowGrammaticalErrors
linktitle: ShowGrammaticalErrors
articleTitle: ShowGrammaticalErrors
second_title: Aspose.Words لـ .NET
description: تحكّم في ظهور الأخطاء النحوية في مستندك باستخدام خاصية "إظهار الأخطاء النحوية". حسّن وضوح الكتابة واحترافيتها بسهولة.
type: docs
weight: 410
url: /ar/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

يحدد ما إذا كان سيتم عرض أخطاء القواعد النحوية في هذا المستند.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

## أمثلة

يوضح كيفية إظهار/إخفاء الأخطاء في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جملتين تحتويان على أخطاء ليتم التقاطها
// بواسطة مدقق الإملاء والقواعد النحوية في Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// إذا تم تمكين هذه الخيارات، فسيتم تسطير الأخطاء الإملائية
// في المستند الناتج بخط أحمر متعرج، وخط أزرق مزدوج يسلط الضوء على الأخطاء النحوية.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
