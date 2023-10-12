---
title: PageSetup.LineNumberRestartMode
second_title: Aspose.Words لمراجع .NET API
description: PageSetup ملكية. الحصول على أو تعيين الطريقة التي يتم بها تشغيل ترقيم الأسطر سواء كان يبدأ من جديد في بداية صفحة أو قسم new أو يتم تشغيله بشكل مستمر.
type: docs
weight: 230
url: /ar/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

الحصول على أو تعيين الطريقة التي يتم بها تشغيل ترقيم الأسطر، سواء كان يبدأ من جديد في بداية صفحة أو قسم new أو يتم تشغيله بشكل مستمر.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

### أمثلة

يوضح كيفية تمكين ترقيم الأسطر لقسم ما.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام كائن PageSetup الخاص بالقسم لعرض الأرقام الموجودة على يسار سطور نص القسم.
// هذا هو نفس سلوك كائن القائمة،
// لكنه يغطي القسم بأكمله ولا يعدل النص بأي شكل من الأشكال.
// سيقوم قسمنا بإعادة تشغيل الترقيم في كل صفحة جديدة من 1 ويعرض الرقم،
// إذا كان من مضاعفات الرقم 3، عند مسافة 50 نقطة على يسار السطر.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// سوف يتخطى عداد السطر أي فقرة مع تعيين علامة "SuppressLineNumbers" على "true".
// هذه الفقرة موجودة في السطر الخامس عشر، وهو من مضاعفات الرقم 3، وبالتالي يتم عرض رقم السطر عادةً.
// عداد سطر القسم سيتجاهل هذا السطر أيضًا، ويعامل السطر التالي باعتباره السطر الخامس عشر،
// ومواصلة العد من تلك النقطة فصاعدا.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### أنظر أيضا

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../pagesetup/)
* المجسم [Aspose.Words](../../../)


