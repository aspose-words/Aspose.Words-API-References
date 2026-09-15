---
title: "طريقة Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty"
linktitle: "get_UpdateLastPrintedProperty"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty. يحصل على أو يعيّن قيمة تحدد ما إذا كانت خاصية LastPrinted يتم تحديثها قبل الحفظ في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words.saving/saveoptions/get_updatelastprintedproperty/
---
## SaveOptions::get_UpdateLastPrintedProperty method


يحصل أو يعيّن قيمة تحدد ما إذا كانت خاصية [LastPrinted](../../../aspose.words.properties/builtindocumentproperties/get_lastprinted/) يتم تحديثها قبل الحفظ.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_UpdateLastPrintedProperty() const
```


## أمثلة



يظهر كيفية تحديث خاصية \"آخر طباعة\" للمستند عند الحفظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::DateTime lastPrinted(2019, 12, 20);
doc->get_BuiltInDocumentProperties()->set_LastPrinted(lastPrinted);

// تحدد هذه العلامة ما إذا كان تاريخ آخر طباعة، وهو خاصية مدمجة، يتم تحديثه.
// إذا كان الأمر كذلك، فإن تاريخ آخر عملية حفظ للمستند
// مع تمرير كائن SaveOptions هذا كمعامل يُستخدم كتاريخ الطباعة.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::DocSaveOptions>();
saveOptions->set_UpdateLastPrintedProperty(isUpdateLastPrintedProperty);

// في Microsoft Word 2003، يمكن العثور على هذه الخاصية عبر ملف -> خصائص -> إحصائيات -> مطبوع.
// يمكن أيضًا عرضها في جسم المستند باستخدام حقل PRINTDATE.
doc->Save(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc", saveOptions);

// افتح المستند المحفوظ، ثم تحقق من قيمة الخاصية.
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"DocSaveOptions.UpdateLastPrintedProperty.doc");

if (isUpdateLastPrintedProperty)
{
    ASSERT_NE(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
else
{
    ASSERT_EQ(lastPrinted, doc->get_BuiltInDocumentProperties()->get_LastPrinted());
}
```

## انظر أيضًا

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
