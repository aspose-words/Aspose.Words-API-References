---
title: Enum LineNumberRestartMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.LineNumberRestartMode تعداد. تحديد وقت إعادة تشغيل ترقيم السطر التلقائي.
type: docs
weight: 3230
url: /ar/net/aspose.words/linenumberrestartmode/
---
## LineNumberRestartMode enumeration

تحديد وقت إعادة تشغيل ترقيم السطر التلقائي.

```csharp
public enum LineNumberRestartMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| RestartPage | `0` | يتم إعادة تشغيل ترقيم الأسطر في بداية كل صفحة. |
| RestartSection | `1` | إعادة تشغيل ترقيم الأسطر في بداية القسم. |
| Continuous | `2` | ترقيم الأسطر مستمر من القسم السابق. |

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

* class [PageSetup](../pagesetup/)
* property [LineNumberRestartMode](../pagesetup/linenumberrestartmode/)
* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)


