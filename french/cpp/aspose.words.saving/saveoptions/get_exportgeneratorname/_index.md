---
title: "Méthode Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName"
linktitle: "get_ExportGeneratorName"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName. Lorsque vrai, insère le nom et la version d'Aspose.Words dans les fichiers générés. La valeur par défaut est vraie en C++."
type: docs
weight: 9000
url: /fr/cpp/aspose.words.saving/saveoptions/get_exportgeneratorname/
---
## SaveOptions::get_ExportGeneratorName method


Lorsque **true**, le nom et la version d'Aspose.Words sont incorporés dans les fichiers produits. La valeur par défaut est **true**.

```cpp
bool Aspose::Words::Saving::SaveOptions::get_ExportGeneratorName() const
```


## Exemples



Montre comment désactiver l'ajout du nom et de la version d'Aspose.Words dans les fichiers générés.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Utilisez https://docs.aspose.com/words/net/generator-or-producer-name-included-in-output-documents/ pour savoir comment vérifier le résultat.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_ExportGeneratorName(false);

doc->Save(get_ArtifactsDir() + u"OoxmlSaveOptions.ExportGeneratorName.docx", saveOptions);
```

## Voir aussi

* Class [SaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
