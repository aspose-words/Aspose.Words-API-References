---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 method"
linktitle: "get_IsStrictSchema11"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11. تحدد ما إذا كان التصدير يجب أن يتوافق بدقة مع مواصفة ODT الإصدار 1.1. يعرض OOo 3.0 الملفات بشكل صحيح عندما تحتوي على عناصر وسمات ODT 1.2. استخدم \"false\" لهذا الغرض، أو \"true\" للامتثال الصارم للمواصفة 1.1. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


يحدد ما إذا كان يجب أن يتطابق التصدير مع مواصفة ODT 1.1 بدقة. يعرض OOo 3.0 الملفات بشكل صحيح عندما تحتوي على عناصر وسمات ODT 1.2. استخدم \"false\" لهذا الغرض، أو \"true\" للامتثال الصارم للمواصفة 1.1. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
```


## أمثلة



يظهر كيفية جعل المستند المحفوظ يتوافق مع مخطط ODT أقدم.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## انظر أيضًا

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
