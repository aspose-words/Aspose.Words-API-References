---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::MeasurementUnits enum. Specifica l'unità di misura in C++."
type: docs
weight: 100000
url: /it/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Specifica l'unità di misura.

```cpp
enum class MeasurementUnits
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Pollici | 0 | Pollici. |
| Centimetri | 1 | Centimetri. |
| Millimetri | 2 | Millimetri. |
| Punti | 3 | Punti. |
| Piche | 4 | Piche (comunemente usate nella spaziatura dei caratteri delle macchine da scrivere tradizionali). |


## Esempi



Mostra come far conformare un documento salvato a uno schema ODT più vecchio.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
