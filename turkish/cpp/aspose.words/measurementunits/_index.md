---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::MeasurementUnits enum. C++'ta ölçü birimini belirtir."
type: docs
weight: 100000
url: /tr/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Ölçü birimini belirtir.

```cpp
enum class MeasurementUnits
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| İnç | 0 | İnç. |
| Santimetre | 1 | Santimetre. |
| Milimetre | 2 | Milimetre. |
| Puan | 3 | Puan. |
| Pika | 4 | Pika (geleneksel daktilo yazı tipi aralığında yaygın olarak kullanılır). |


## Örnekler



Kaydedilmiş bir belgenin eski bir ODT şemasına uygun hale getirilmesini gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Ayrıca Bakınız

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
