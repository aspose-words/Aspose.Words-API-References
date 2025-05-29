---
title: LineNumberRestartMode Enum
linktitle: LineNumberRestartMode
articleTitle: LineNumberRestartMode
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.LineNumberRestartMode للتحكم في إعادة تعيين ترقيم الأسطر تلقائيًا لتحسين تنسيق المستندات ووضوحها.
type: docs
weight: 3880
url: /ar/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

يحدد متى يتم إعادة تشغيل ترقيم الأسطر التلقائي.

```csharp
public enum LineNumberRestartMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| RestartPage | `0` | يتم إعادة تشغيل ترقيم الأسطر في بداية كل صفحة. |
| RestartSection | `1` | يتم إعادة تشغيل ترقيم الأسطر عند بداية القسم. |
| Continuous | `2` | ترقيم الأسطر مستمر من القسم السابق. |

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
