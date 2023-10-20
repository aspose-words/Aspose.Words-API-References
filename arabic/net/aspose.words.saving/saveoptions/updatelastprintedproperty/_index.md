---
title: SaveOptions.UpdateLastPrintedProperty
linktitle: UpdateLastPrintedProperty
articleTitle: UpdateLastPrintedProperty
second_title: Aspose.Words لـ .NET
description: SaveOptions UpdateLastPrintedProperty ملكية. الحصول على أو تعيين قيمة لتحديد ما إذا كانLastPrinted يتم تحديث الخاصية قبل الحفظ في C#.
type: docs
weight: 170
url: /ar/net/aspose.words.saving/saveoptions/updatelastprintedproperty/
---
## SaveOptions.UpdateLastPrintedProperty property

الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastPrinted`](../../../aspose.words.properties/builtindocumentproperties/lastprinted/) يتم تحديث الخاصية قبل الحفظ.

```csharp
public bool UpdateLastPrintedProperty { get; set; }
```

## أمثلة

يوضح كيفية تحديث خاصية "CreatedTime" للمستند عند الحفظ.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.CreatedTime = new DateTime(2019, 12, 20);

// تحدد هذه العلامة ما إذا كان الوقت الذي تم إنشاؤه، وهو خاصية مضمنة، قد تم تحديثه أم لا.
// إذا كان الأمر كذلك، فهذا يعني تاريخ آخر عملية حفظ للمستند
// مع تمرير كائن SaveOptions هذا كمعلمة، يتم استخدامه كوقت الإنشاء.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// افتح المستند المحفوظ، ثم تحقق من قيمة الخاصية.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

Assert.AreNotEqual(isUpdateCreatedTimeProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.CreatedTime);
```

يوضح كيفية تحديث خاصية "آخر طباعة" للمستند عند الحفظ.

```csharp
Document doc = new Document();
doc.BuiltInDocumentProperties.LastPrinted = new DateTime(2019, 12, 20);

// تحدد هذه العلامة ما إذا كان تاريخ الطباعة الأخير، وهو خاصية مضمنة، قد تم تحديثه.
// إذا كان الأمر كذلك، فهذا يعني تاريخ آخر عملية حفظ للمستند
// مع تمرير كائن SaveOptions هذا كمعلمة، يتم استخدامه كتاريخ الطباعة.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateLastPrintedProperty = isUpdateLastPrintedProperty;

// في Microsoft Word 2003، يمكن العثور على هذه الخاصية عبر File -> الخصائص -> إحصائيات -> مطبوعة.
// يمكن أيضًا عرضه في نص المستند باستخدام حقل PRINTDATE.
doc.Save(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// افتح المستند المحفوظ، ثم تحقق من قيمة الخاصية.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateLastPrintedProperty.doc");

Assert.AreNotEqual(isUpdateLastPrintedProperty, new DateTime(2019, 12, 20) == doc.BuiltInDocumentProperties.LastPrinted);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
