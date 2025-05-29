---
title: PageSetup.LineNumberRestartMode
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup LineNumberRestartMode للتحكم في ترقيم الأسطر—اختر بين إعادة التشغيل في الصفحات الجديدة أو الترقيم المستمر للمستندات المترابطة.
type: docs
weight: 230
url: /ar/net/aspose.words/pagesetup/linenumberrestartmode/
---
## PageSetup.LineNumberRestartMode property

يحصل على طريقة تشغيل ترقيم الأسطر أو يحددها، أي ما إذا كان يبدأ من جديد في بداية صفحة أو قسم جديد أو يعمل بشكل مستمر.

```csharp
public LineNumberRestartMode LineNumberRestartMode { get; set; }
```

## أمثلة

يوضح كيفية تمكين ترقيم الأسطر لقسم ما.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// يمكننا استخدام كائن PageSetup الخاص بالقسم لعرض الأرقام على يسار أسطر نص القسم.
// هذا هو نفس سلوك كائن القائمة،
// لكنه يغطي القسم بأكمله ولا يعدل النص بأي شكل من الأشكال.
// سيقوم قسمنا بإعادة تشغيل الترقيم في كل صفحة جديدة من 1 وعرض الرقم،
// إذا كان مضاعفًا لـ 3، عند 50 نقطة إلى يسار السطر.
PageSetup pageSetup = builder.PageSetup;
pageSetup.LineStartingNumber = 1;
pageSetup.LineNumberCountBy = 3;
pageSetup.LineNumberRestartMode = LineNumberRestartMode.RestartPage;
pageSetup.LineNumberDistanceFromText = 50.0d;

for (int i = 1; i <= 25; i++)
    builder.Writeln($"Line {i}.");

// سوف يتخطى عداد الأسطر أي فقرة يتم فيها تعيين العلم "SuppressLineNumbers" على "true".
//تقع هذه الفقرة في السطر الخامس عشر، وهو مضاعف للرقم 3، وبالتالي من الطبيعي أن تعرض رقم السطر.
// سوف يتجاهل عداد أسطر القسم هذا السطر أيضًا، ويعامل السطر التالي على أنه السطر الخامس عشر،
// واستمر في العد من تلك النقطة فصاعدًا.
doc.FirstSection.Body.Paragraphs[14].ParagraphFormat.SuppressLineNumbers = true;

doc.Save(ArtifactsDir + "PageSetup.LineNumbers.docx");
```

### أنظر أيضا

* enum [LineNumberRestartMode](../../linenumberrestartmode/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
