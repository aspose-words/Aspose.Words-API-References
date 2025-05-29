---
title: AdvancedCompareOptions.IgnoreDmlUniqueId
linktitle: IgnoreDmlUniqueId
articleTitle: IgnoreDmlUniqueId
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية AdvancedCompareOptions IgnoreDmlUniqueId لتحسين معالجة DrawingML من خلال إدارة معرفات فريدة بكفاءة. حسّن سير عملك!
type: docs
weight: 20
url: /ar/net/aspose.words.comparing/advancedcompareoptions/ignoredmluniqueid/
---
## AdvancedCompareOptions.IgnoreDmlUniqueId property

يحدد ما إذا كان سيتم تجاهل الاختلاف في معرف DrawingML الفريد.

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

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

* class [AdvancedCompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../../aspose.words.comparing/)
* المجسم [Aspose.Words](../../../)
