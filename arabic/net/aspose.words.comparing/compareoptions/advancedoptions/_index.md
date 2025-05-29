---
title: CompareOptions.AdvancedOptions
linktitle: AdvancedOptions
articleTitle: AdvancedOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات CompareOptions المتقدمة لتحسين مقارناتك. حقق نتائج دقيقة بإعدادات مُخصصة لتحقيق أفضل النتائج.
type: docs
weight: 20
url: /ar/net/aspose.words.comparing/compareoptions/advancedoptions/
---
## CompareOptions.AdvancedOptions property

يحدد خيارات المقارنة المتقدمة التي قد تساعد في إنتاج مخرجات مقارنة أكثر دقة.

```csharp
public AdvancedCompareOptions AdvancedOptions { get; }
```

## أمثلة

يوضح كيفية مقارنة المستندات مع تجاهل معرف DML الفريد.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// بشكل افتراضي، لا يتجاهل Aspose.Words معرف DML الفريد، وكان عدد المراجعات 2.
// إذا كنا نتجاهل معرف DML الفريد، وكان عدد المراجعات 0.
CompareOptions compareOptions = new CompareOptions();
compareOptions.AdvancedOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### أنظر أيضا

* class [AdvancedCompareOptions](../../advancedcompareoptions/)
* class [CompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../../)
