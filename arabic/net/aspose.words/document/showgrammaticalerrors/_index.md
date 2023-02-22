---
title: Document.ShowGrammaticalErrors
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. تحديد ما إذا كان سيتم عرض الأخطاء النحوية في هذا المستند.
type: docs
weight: 370
url: /ar/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

تحديد ما إذا كان سيتم عرض الأخطاء النحوية في هذا المستند.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

### أمثلة

يوضح كيفية إظهار / إخفاء الأخطاء في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جملتين مع الأخطاء التي سيتم التقاطها
// بواسطة المدققات الإملائية والنحوية في Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// إذا تم تمكين هذه الخيارات ، فسيتم وضع خط تحت الأخطاء الإملائية
// في مستند الإخراج بخط أحمر متعرج ، وخط أزرق مزدوج يبرز الأخطاء النحوية.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


