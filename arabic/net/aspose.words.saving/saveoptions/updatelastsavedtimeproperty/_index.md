---
title: SaveOptions.UpdateLastSavedTimeProperty
linktitle: UpdateLastSavedTimeProperty
articleTitle: UpdateLastSavedTimeProperty
second_title: Aspose.Words لـ .NET
description: حسّن خيارات الحفظ لديك باستخدام خاصية UpdateLastSavedTime. تحكّم بتحديثات LastSavedTime لإدارة بيانات فعّالة وتحسين الأداء.
type: docs
weight: 190
url: /ar/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

يحصل على قيمة أو يعينها لتحديد ما إذا كان[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

## أمثلة

يوضح كيفية تحديد ما إذا كان سيتم الحفاظ على خاصية "آخر وقت حفظ" للمستند عند الحفظ.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// عندما نحفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم قم بتمريرها إلى طريقة حفظ المستند لتعديل كيفية حفظ المستند.
// اضبط خاصية "UpdateLastSavedTimeProperty" على "true" لـ
// تعيين خاصية "آخر وقت تم حفظه" المضمنة في مستند الإخراج إلى التاريخ/الوقت الحالي.
// اضبط خاصية "UpdateLastSavedTimeProperty" على "false"
// الحفاظ على القيمة الأصلية لخاصية "آخر وقت تم حفظه" المضمنة في مستند الإدخال.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.IsTrue((DateTime.Now - lastSavedTimeNew).Days < 1);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
