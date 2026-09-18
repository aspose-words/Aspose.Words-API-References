---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::MeasurementUnits enum. Gibt die Einheit der Messung in C++ an."
type: docs
weight: 100000
url: /de/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Gibt die Maßeinheit an.

```cpp
enum class MeasurementUnits
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Zoll | 0 | Zoll. |
| Zentimeter | 1 | Zentimeter. |
| Millimeter | 2 | Millimeter. |
| Punkte | 3 | Punkte. |
| Picas | 4 | Picas (häufig verwendet bei traditioneller Schreibmaschinenschrift). |


## Beispiele



Zeigt, wie ein gespeichertes Dokument an ein älteres ODT-Schema angepasst wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
