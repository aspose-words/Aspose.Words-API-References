---
title: PageSetup.LineNumberRestartMode
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. الحصول على طريقة تشغيل ترقيم الأسطر أو تعيينها  سواء كانت تبدأ من جديد في بداية صفحة أو قسم جديد أو يتم تشغيلها بشكل مستمر.
type: docs
weight: 230
url: /ar/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

الحصول على طريقة تشغيل ترقيم الأسطر أو تعيينها ، سواء كانت تبدأ من جديد في بداية صفحة أو قسم جديد أو يتم تشغيلها بشكل مستمر.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

### أمثلة

يوضح كيفية تمكين ترقيم الأسطر لقسم.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام كائن PageSetup للقسم لعرض الأرقام على يسار سطور نص القسم.
// هذا هو نفس سلوك كائن القائمة ،
// ولكنه يغطي القسم بأكمله ولا يقوم بتعديل النص بأي شكل من الأشكال.
// سيقوم قسمنا بإعادة الترقيم في كل صفحة جديدة من 1 وعرض الرقم ،
// إذا كان من مضاعفات العدد 3 ، عند 50 نقطة على يسار السطر.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// سيتخطى عداد الأسطر أي فقرة مع تعيين علامة "SuppressLineNumbers" على "true".
// هذه الفقرة موجودة في السطر الخامس عشر ، وهي من مضاعفات العدد 3 ، وبالتالي فإنها تعرض رقم السطر بشكل طبيعي.
// سيتجاهل عداد سطر القسم أيضًا هذا السطر ، ويعامل السطر التالي على أنه السطر الخامس عشر ،
// واستمر في العد من تلك النقطة فصاعدًا.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### أنظر أيضا

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


