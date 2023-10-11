---
title: CompareOptions.Granularity
second_title: Aspose.Words لمراجع .NET API
description: CompareOptions ملكية. يحدد ما إذا كان سيتم تعقب التغييرات حسب الحرف أو الكلمة. القيمة الافتراضية هيWordLevel .
type: docs
weight: 30
url: /ar/net/aspose.words.comparing/compareoptions/granularity/
---
## CompareOptions.Granularity property

يحدد ما إذا كان سيتم تعقب التغييرات حسب الحرف أو الكلمة. القيمة الافتراضية هيWordLevel .

```csharp
public Granularity Granularity { get; set; }
```

### أمثلة

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

* enum [Granularity](../../granularity/)
* class [CompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../compareoptions/)
* المجسم [Aspose.Words](../../../)


