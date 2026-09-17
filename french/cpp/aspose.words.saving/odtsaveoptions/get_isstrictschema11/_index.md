---
title: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 méthode"
linktitle: "get_IsStrictSchema11"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11 méthode. Spécifie si l'exportation doit correspondre strictement à la spécification ODT 1.1. OOo 3.0 affiche correctement les fichiers lorsqu'ils contiennent des éléments et des attributs de l'ODT 1.2. Utilisez \"false\" à cet effet, ou \"true\" pour une conformité stricte à la spécification 1.1. La valeur par défaut est false en C++."
type: docs
weight: 3000
url: /fr/cpp/aspose.words.saving/odtsaveoptions/get_isstrictschema11/
---
## OdtSaveOptions::get_IsStrictSchema11 method


Spécifie si l'exportation doit correspondre strictement à la spécification ODT 1.1. OOo 3.0 affiche correctement les fichiers lorsqu'ils contiennent des éléments et attributs de ODT 1.2. Utilisez "false" à cet effet, ou "true" pour une conformité stricte à la spécification 1.1. La valeur par défaut est **false**.

```cpp
bool Aspose::Words::Saving::OdtSaveOptions::get_IsStrictSchema11() const
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

* Class [OdtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
