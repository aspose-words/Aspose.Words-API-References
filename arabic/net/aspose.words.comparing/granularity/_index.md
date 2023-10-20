---
title: Granularity Enum
linktitle: Granularity
articleTitle: Granularity
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Comparing.Granularity تعداد. يحدد مدى دقة التغييرات التي يجب تتبعها عند مقارنة مستندين في C#.
type: docs
weight: 290
url: /ar/net/aspose.words.comparing/granularity/
---
## Granularity enumeration

يحدد مدى دقة التغييرات التي يجب تتبعها عند مقارنة مستندين.

```csharp
public enum Granularity
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| CharLevel | `0` |  |
| WordLevel | `1` |  |

## أمثلة

يظهر لتحديد التفاصيل أثناء مقارنة المستندات.

```csharp
Document docA = new Document();
DocumentBuilder builderA = new DocumentBuilder(docA);
builderA.Writeln("Alpha Lorem ipsum dolor sit amet, consectetur adipiscing elit");

Document docB = new Document();
DocumentBuilder builderB = new DocumentBuilder(docB);
builderB.Writeln("Lorems ipsum dolor sit amet consectetur - \"adipiscing\" elit");

// تحديد ما إذا كان سيتم تتبع التغييرات أم لا
// حسب الحرف ('Granularity.CharLevel')، أو حسب الكلمة ('Granularity.WordLevel').
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.Granularity = granularity;

docA.Compare(docB, "author", DateTime.Now, compareOptions);

// تحتوي مجموعة مجموعات المراجعة الخاصة بالمستند الأول على جميع الاختلافات بين المستندات.
RevisionGroupCollection groups = docA.Revisions.Groups;
Assert.AreEqual(5, groups.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Comparing](../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../)
