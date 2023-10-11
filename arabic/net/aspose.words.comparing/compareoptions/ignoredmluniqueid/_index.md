---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Aspose.Words لمراجع .NET API
description: CompareOptions ملكية. يحدد ما إذا كان سيتم تجاهل الاختلاف في المعرف الفريد لـ DrawML. القيمة الافتراضية هيخطأ شنيع .
type: docs
weight: 60
url: /ar/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

يحدد ما إذا كان سيتم تجاهل الاختلاف في المعرف الفريد لـ DrawML. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### أمثلة

يوضح كيفية مقارنة المستندات التي تتجاهل معرف DML الفريد.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// بشكل افتراضي، لا تتجاهل Aspose.Words المعرف الفريد لـ DML، وكان عدد المراجعات 2.
// إذا كنا نتجاهل المعرف الفريد لـ DML، وكان عدد المراجعات 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### أنظر أيضا

* class [CompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../compareoptions/)
* المجسم [Aspose.Words](../../../)


