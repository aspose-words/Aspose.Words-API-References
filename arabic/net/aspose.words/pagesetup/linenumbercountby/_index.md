---
title: PageSetup.LineNumberCountBy
linktitle: LineNumberCountBy
articleTitle: LineNumberCountBy
second_title: Aspose.Words لـ .NET
description: PageSetup LineNumberCountBy ملكية. إرجاع أو تعيين الزيادة الرقمية لأرقام الأسطر في C#.
type: docs
weight: 210
url: /ar/net/aspose.words/pagesetup/linenumbercountby/
---
## PageSetup.LineNumberCountBy property

إرجاع أو تعيين الزيادة الرقمية لأرقام الأسطر.

```csharp
public int LineNumberCountBy { get; set; }
```

## أمثلة

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

* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
