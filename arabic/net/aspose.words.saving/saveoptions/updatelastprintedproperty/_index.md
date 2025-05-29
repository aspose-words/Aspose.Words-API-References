---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words لـ .NET
description: حسّن إدارة المستندات باستخدام SaveOptions UpdateLastPrintedProperty. تحكّم بتحديثات LastPrinted لضمان الحفظ الفعال وتحسين سير العمل.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## أمثلة

يوضح كيفية تحديث خاصية "آخر طباعة" للمستند عند الحفظ.

```csharp
Document doc = new Document();

DateTime lastPrinted = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.LastPrinted = lastPrinted;

// يحدد هذا العلم ما إذا كان تاريخ الطباعة الأخير، وهو خاصية مضمنة، سيتم تحديثه.
// إذا كان الأمر كذلك، فسيتم تحديد تاريخ أحدث عملية حفظ للمستند
// مع هذا الكائن SaveOptions الذي تم تمريره كمعلمة يتم استخدامه كتاريخ للطباعة.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// في Microsoft Word 2003، يمكن العثور على هذه الخاصية عبر ملف -> خصائص -> إحصائيات -> مطبوع.
//يمكن أيضًا عرضه في نص المستند باستخدام حقل PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// افتح المستند المحفوظ، ثم تحقق من قيمة الخاصية.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
    Assert.AreNotEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
else
    Assert.AreEqual(lastPrinted, doc.BuiltInDocumentProperties.LastPrinted);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
