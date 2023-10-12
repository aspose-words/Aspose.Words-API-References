---
title: SaveOptions.UpdateLastSavedTimeProperty
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على أو تعيين قيمة لتحديد ما إذا كانLastSavedTime يتم تحديث الخاصية قبل الحفظ.
type: docs
weight: 180
url: /ar/net/aspose.words.saving/saveoptions/updatelastsavedtimeproperty/
---
## SaveOptions.UpdateLastSavedTimeProperty property

الحصول على أو تعيين قيمة لتحديد ما إذا كان[`LastSavedTime`](../../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) يتم تحديث الخاصية قبل الحفظ.

```csharp
public bool UpdateLastSavedTimeProperty { get; set; }
```

### أمثلة

يوضح كيفية تحديد ما إذا كان سيتم الاحتفاظ بخاصية "آخر وقت تم حفظه" للمستند عند الحفظ.

```csharp
Document doc = new Document(MyDir + "Document.docx");

Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
    doc.BuiltInDocumentProperties.LastSavedTime);

// عندما نحفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم قم بتمريره إلى طريقة حفظ المستند لتعديل كيفية حفظ المستند.
// قم بتعيين خاصية "UpdateLastSavedTimeProperty" على "صحيح" لـ
// قم بتعيين الخاصية المضمنة "آخر وقت تم حفظه" للمستند الناتج على التاريخ/الوقت الحالي.
// قم بتعيين خاصية "UpdateLastSavedTimeProperty" على "خطأ" لـ
// الحفاظ على القيمة الأصلية للخاصية المضمنة "آخر وقت تم حفظه" في مستند الإدخال.
OoxmlSaveOptions saveOptions = new OoxmlSaveOptions();
saveOptions.UpdateLastSavedTimeProperty = updateLastSavedTimeProperty;

doc.Save(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = new Document(ArtifactsDir + "OoxmlSaveOptions.LastSavedTime.docx");
DateTime lastSavedTimeNew = doc.BuiltInDocumentProperties.LastSavedTime;

if (updateLastSavedTimeProperty)
    Assert.That(DateTime.Now, Is.EqualTo(lastSavedTimeNew).Within(1).Days);
else
    Assert.AreEqual(new DateTime(2021, 5, 11, 6, 32, 0), 
        lastSavedTimeNew);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


