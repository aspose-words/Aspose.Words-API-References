---
title: "Aspose::Words::MeasurementUnits enum"
linktitle: "MeasurementUnits"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Enum Aspose::Words::MeasurementUnits. Spécifie l'unité de mesure en C++."
type: docs
weight: 100000
url: /fr/cpp/aspose.words/measurementunits/
---
## MeasurementUnits enum


Spécifie l'unité de mesure.

```cpp
enum class MeasurementUnits
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Pouces | 0 | Pouces. |
| Centimètres | 1 | Centimètres. |
| Millimètres | 2 | Millimètres. |
| Points | 3 | Points. |
| Picas | 4 | Picas (souvent utilisés dans l'espacement de police des machines à écrire traditionnelles). |


## Exemples



Montre comment faire en sorte qu'un document enregistré se conforme à un schéma ODT plus ancien.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>();
saveOptions->set_MeasureUnit(Aspose::Words::Saving::OdtSaveMeasureUnit::Centimeters);
saveOptions->set_IsStrictSchema11(exportToOdt11Specs);

doc->Save(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt", saveOptions);

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"OdtSaveOptions.Odt11Schema.odt");
ASSERT_EQ(Aspose::Words::MeasurementUnits::Centimeters, doc->get_LayoutOptions()->get_RevisionOptions()->get_MeasurementUnit());
```

## Voir aussi

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
