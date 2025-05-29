---
title: Document.ShowSpellingErrors
linktitle: ShowSpellingErrors
articleTitle: ShowSpellingErrors
second_title: Aspose.Words لـ .NET
description: تحكّم في ظهور الأخطاء الإملائية في مستندك باستخدام خاصية "إظهار الأخطاء الإملائية". حسّن عملية التحرير وحسّن جودة المستند.
type: docs
weight: 420
url: /ar/net/aspose.words/document/showspellingerrors/
---
## Document.ShowSpellingErrors property

يحدد ما إذا كان سيتم عرض الأخطاء الإملائية في هذا المستند.

```csharp
public bool ShowSpellingErrors { get; set; }
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
