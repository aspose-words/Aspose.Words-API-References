---
title: Document.ShowGrammaticalErrors
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يحدد ما إذا كان سيتم عرض الأخطاء النحوية في هذا المستند.
type: docs
weight: 390
url: /ar/net/aspose.words/document/showgrammaticalerrors/
---
## Document.ShowGrammaticalErrors property

يحدد ما إذا كان سيتم عرض الأخطاء النحوية في هذا المستند.

```csharp
public bool ShowGrammaticalErrors { get; set; }
```

### أمثلة

يوضح كيفية إظهار/إخفاء الأخطاء في المستند.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// أدخل جملتين بها أخطاء يمكن التقاطها
// بواسطة المدققين الإملائي والنحوي في Microsoft Word.
builder.Writeln("There is a speling error in this sentence.");
builder.Writeln("Their is a grammatical error in this sentence.");

// إذا تم تمكين هذه الخيارات، فسيتم وضع خط تحت الأخطاء الإملائية
// في مستند الإخراج بواسطة خط أحمر متعرج، وسيقوم الخط الأزرق المزدوج بتسليط الضوء على الأخطاء النحوية.
doc.ShowGrammaticalErrors = showErrors;
doc.ShowSpellingErrors = showErrors;

doc.Save(ArtifactsDir + "Document.SpellingAndGrammarErrors.docx");
```

### أنظر أيضا

* class [Document](../)
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


