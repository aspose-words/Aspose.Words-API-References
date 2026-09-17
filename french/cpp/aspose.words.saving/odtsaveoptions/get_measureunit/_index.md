---
title: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit méthode"
linktitle: "get_MeasureUnit"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit méthode. Permet de spécifier les unités de mesure à appliquer au contenu du document. La valeur par défaut est Centimeters en C++."
type: docs
weight: 4000
url: /fr/cpp/aspose.words.saving/odtsaveoptions/get_measureunit/
---
## OdtSaveOptions::get_MeasureUnit method


Permet de spécifier les unités de mesure à appliquer au contenu du document. La valeur par défaut est [Centimeters](../../odtsavemeasureunit/)

```cpp
Aspose::Words::Saving::OdtSaveMeasureUnit Aspose::Words::Saving::OdtSaveOptions::get_MeasureUnit() const
```


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

* Enum [OdtSaveMeasureUnit](../../odtsavemeasureunit/)
* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
