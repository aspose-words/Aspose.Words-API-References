---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::MeasurementUnits enum. Anger enheten för mätning i C++."
type: docs
weight: 100000
url: /sv/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Anger mätenheten.

```cpp
enum class MeasurementUnits
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Tum | 0 | Tum. |
| Centimeter | 1 | Centimeter. |
| Millimeter | 2 | Millimeter. |
| Punkter | 3 | Punkter. |
| Picas | 4 | Picas (vanligtvis använda i traditionell skrivmaskins teckensnittsavstånd). |


## Exempel



Visar hur man får ett sparat dokument att följa ett äldre ODT-schema.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Se även

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
