---
title: CompareOptions.IgnoreDmlUniqueId
second_title: Aspose.Words لمراجع .NET API
description: CompareOptions ملكية. يحدد ما إذا كان سيتم تجاهل الاختلاف في معرّف DrawingML الفريد. القيمة الافتراضية هي خاطئة .
type: docs
weight: 50
url: /ar/net/aspose.words.comparing/compareoptions/ignoredmluniqueid/
---
## CompareOptions.IgnoreDmlUniqueId property

يحدد ما إذا كان سيتم تجاهل الاختلاف في معرّف DrawingML الفريد. القيمة الافتراضية هي **خاطئة** .

```csharp
public bool IgnoreDmlUniqueId { get; set; }
```

### أمثلة

يوضح كيفية مقارنة المستندات التي تتجاهل معرّف DML الفريد.

```csharp
Document docA = new Document(MyDir + "DML unique ID original.docx");
Document docB = new Document(MyDir + "DML unique ID compare.docx");

// افتراضيًا ، لا تتجاهل Aspose.Words معرّف DML الفريد ، وكان عدد المراجعات 2.
// إذا كنا نتجاهل المعرف الفريد لـ DML ، وكان عدد المراجعات 0.
Aspose.Words.Comparing.CompareOptions compareOptions = new Aspose.Words.Comparing.CompareOptions();
compareOptions.IgnoreDmlUniqueId = isIgnoreDmlUniqueId;

docA.Compare(docB, "Aspose.Words", DateTime.Now, compareOptions);

Assert.AreEqual(isIgnoreDmlUniqueId ? 0 : 2, docA.Revisions.Count);
```

### أنظر أيضا

* class [CompareOptions](../)
* مساحة الاسم [Aspose.Words.Comparing](../../compareoptions/)
* المجسم [Aspose.Words](../../../)


