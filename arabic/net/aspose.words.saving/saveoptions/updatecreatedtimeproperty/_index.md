---
title: SaveOptions.UpdateCreatedTimeProperty
linktitle: UpdateCreatedTimeProperty
articleTitle: UpdateCreatedTimeProperty
second_title: Aspose.Words لـ .NET
description: حسّن خيارات الحفظ باستخدام خاصية UpdateCreatedTimeProperty. تحكّم في تحديثات CreatedTime قبل الحفظ، مما يُحسّن دقة البيانات. الافتراضي: خطأ.
type: docs
weight: 160
url: /ar/net/aspose.words.saving/saveoptions/updatecreatedtimeproperty/
---
## SaveOptions.UpdateCreatedTimeProperty property

يحصل على قيمة أو يعينها لتحديد ما إذا كان[`CreatedTime`](../../../aspose.words.properties/builtindocumentproperties/createdtime/) يتم تحديث الخاصية قبل الحفظ. القيمة الافتراضية هي`خطأ شنيع` ;

```csharp
public bool UpdateCreatedTimeProperty { get; set; }
```

## أمثلة

يوضح كيفية تحديث خاصية "CreatedTime" الخاصة بالمستند عند الحفظ.

```csharp
Document doc = new Document();

DateTime createdTime = new DateTime(2019, 12, 20);
doc.BuiltInDocumentProperties.CreatedTime = createdTime;

// يحدد هذا العلم ما إذا كان الوقت الذي تم إنشاؤه، والذي يعد خاصية مضمنة، سيتم تحديثه.
// إذا كان الأمر كذلك، فسيتم تحديد تاريخ أحدث عملية حفظ للمستند
// مع هذا الكائن SaveOptions الذي تم تمريره كمعلمة يتم استخدامه كوقت الإنشاء.
DocSaveOptions saveOptions = new DocSaveOptions();
saveOptions.UpdateCreatedTimeProperty = isUpdateCreatedTimeProperty;

doc.Save(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// افتح المستند المحفوظ، ثم تحقق من قيمة الخاصية.
doc = new Document(ArtifactsDir + "DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
    Assert.AreNotEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
else
    Assert.AreEqual(createdTime, doc.BuiltInDocumentProperties.CreatedTime);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
