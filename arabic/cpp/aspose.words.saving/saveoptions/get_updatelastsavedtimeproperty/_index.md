---
title: "طريقة Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty"
linktitle: "get_UpdateLastSavedTimeProperty"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty. يحصل على أو يعيّن قيمة تحدد ما إذا كانت الخاصية LastSavedTime يتم تحديثها قبل الحفظ في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.saving/saveoptions/get_updatelastsavedtimeproperty/
---
## SaveOptions::get_UpdateLastSavedTimeProperty method


يحصل على أو يعيّن قيمة تحدد ما إذا كانت الخاصية [LastSavedTime](../../../aspose.words.properties/builtindocumentproperties/get_lastsavedtime/) يتم تحديثها قبل الحفظ.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastSavedTimeProperty() const
```


## أمثلة



يوضح كيفية تحديد ما إذا كان يجب الحفاظ على خاصية "Last saved time" للمستند عند الحفظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Document.docx");

ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), doc->get_BuiltInDocumentProperties()->get_LastSavedTime());

// عند حفظ المستند بتنسيق OOXML، يمكننا إنشاء كائن OoxmlSaveOptions
// ثم نمرره إلى طريقة حفظ المستند لتعديل طريقة حفظ المستند.
// قم بتعيين الخاصية "UpdateLastSavedTimeProperty" إلى "true" لت
// تعيين الخاصية المدمجة "Last saved time" للمستند الناتج إلى التاريخ/الوقت الحالي.
// قم بتعيين الخاصية "UpdateLastSavedTimeProperty" إلى "false" لت
// الحفاظ على القيمة الأصلية للخاصية المدمجة "Last saved time" للمستند المدخل.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_UpdateLastSavedTimeProperty(updateLastSavedTimeProperty);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OoxmlSaveOptions.LastSavedTime.docx");
System::DateTime lastSavedTimeNew = doc->get_BuiltInDocumentProperties()->get_LastSavedTime();

if (updateLastSavedTimeProperty)
{
    ASSERT_TRUE((System::DateTime::get_Now() - lastSavedTimeNew).get_Days() < 1);
}
else
{
    ASSERT_EQ(System::DateTime(2021, 5, 11, 6, 32, 0), lastSavedTimeNew);
}
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
