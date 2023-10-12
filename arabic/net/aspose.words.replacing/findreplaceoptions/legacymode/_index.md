---
title: FindReplaceOptions.LegacyMode
second_title: Aspose.Words لمراجع .NET API
description: FindReplaceOptions ملكية. الحصول على قيمة منطقية أو تعيينها تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة.
type: docs
weight: 130
url: /ar/net/aspose.words.replacing/findreplaceoptions/legacymode/
---
## FindReplaceOptions.LegacyMode property

الحصول على قيمة منطقية أو تعيينها تشير إلى استخدام خوارزمية البحث/الاستبدال القديمة.

```csharp
public bool LegacyMode { get; set; }
```

### ملاحظات

استخدم هذه العلامة إذا كنت بحاجة إلى نفس السلوك تمامًا كما كان قبل تقديم ميزة البحث/الاستبدال المتقدمة. لاحظ أن الخوارزمية القديمة لا تدعم الميزات المتقدمة مثل الاستبدال بالفواصل وتطبيق التنسيق وما إلى ذلك.

### أمثلة

يوضح كيفية التعرف على البدائل واستخدامها ضمن أنماط الاستبدال.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Jason gave money to Paul.");

Regex regex = new Regex(@"([A-z]+) gave money to ([A-z]+)");

FindReplaceOptions options = new FindReplaceOptions();
options.UseSubstitutions = true;

// استخدام الوضع القديم لا يدعم العديد من الميزات المتقدمة، لذا نحتاج إلى ضبطه على "خطأ".
options.LegacyMode = false;

doc.Range.Replace(regex, @"$2 took money from $1", options);

Assert.AreEqual(doc.GetText(), "Paul took money from Jason.\f");
```

### أنظر أيضا

* class [FindReplaceOptions](../)
* مساحة الاسم [Aspose.Words.Replacing](../../findreplaceoptions/)
* المجسم [Aspose.Words](../../../)


