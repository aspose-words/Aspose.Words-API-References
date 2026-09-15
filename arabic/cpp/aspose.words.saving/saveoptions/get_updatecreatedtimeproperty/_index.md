---
title: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty method"
linktitle: "get_UpdateCreatedTimeProperty"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty method. يحصل على أو يحدد قيمة تحدد ما إذا كانت خاصية CreatedTime تُحدَّث قبل الحفظ. القيمة الافتراضية هي false; في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.saving/saveoptions/get_updatecreatedtimeproperty/
---
## SaveOptions::get_UpdateCreatedTimeProperty method


يحصل أو يحدد قيمة تحدد ما إذا كانت خاصية [CreatedTime](../../../aspose.words.properties/builtindocumentproperties/get_createdtime/) تُحدَّث قبل الحفظ. القيمة الافتراضية هي **false**;.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateCreatedTimeProperty() const
```


## أمثلة



يوضح كيفية تحديث خاصية "CreatedTime" للمستند عند الحفظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime createdTime(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_CreatedTime(createdTime);

// تحدد هذه العلامة ما إذا كان وقت الإنشاء، وهو خاصية مدمجة، يتم تحديثه.
// إذا كان الأمر كذلك، فإن تاريخ آخر عملية حفظ للمستند
// مع تمرير كائن SaveOptions هذا كمعامل يُستخدم كوقت الإنشاء.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateCreatedTimeProperty(isUpdateCreatedTimeProperty);

doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx", saveOptions);

// افتح المستند المحفوظ، ثم تحقق من قيمة الخاصية.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateCreatedTimeProperty.docx");

if (isUpdateCreatedTimeProperty)
{
    ASSERT_NE(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
else
{
    ASSERT_EQ(createdTime, doc->get_BuiltInDocumentProperties()->get_CreatedTime());
}
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
