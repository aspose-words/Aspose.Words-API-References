---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words لـ .NET
description: اكتشف أداة Aspose.Words.Comparing.Granularity enum لتتبع تغييرات المستندات بدقة وسهولة. حسّن مقارنة مستنداتك اليوم!
type: docs
weight: 490
url: /ar/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

يحدد تفاصيل التغييرات التي يجب تتبعها عند مقارنة مستندين.

```csharp
public enum Granularity
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| CharLevel | `0` | يحدد التغييرات على مستوى الحرف. |
| WordLevel | `1` | يحدد التغييرات على مستوى الكلمة. |

## أمثلة

يظهر لتحديد الحبيبات أثناء مقارنة المستندات.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// حدد ما إذا كانت التغييرات تتبع
// حسب الحرف ('Granularity.CharLevel')، أو حسب الكلمة ('Granularity.WordLevel').
CompareOptions compareOptions = new CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// تحتوي مجموعة المراجعات الخاصة بالمستند الأول على كافة الاختلافات بين المستندات.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Comparing](../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../)
