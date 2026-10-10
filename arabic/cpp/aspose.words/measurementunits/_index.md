---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::MeasurementUnits enum. يحدد وحدة القياس في C++."
type: docs
weight: 100000
url: /ar/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


يحدد وحدة القياس.

```cpp
enum class MeasurementUnits
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| بوصات | 0 | بوصات. |
| سنتيمترات | 1 | سنتيمترات. |
| ملليمترات | 2 | ملليمترات. |
| نقاط | 3 | نقاط. |
| بيكات | 4 | بيكات (تُستخدم عادةً في تباعد خطوط الآلة الكاتبة التقليدية). |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
