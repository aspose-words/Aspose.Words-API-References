---
title: "Aspose::Words::Saving::XlsxSectionMode enum"
linktitle: "XlsxSectionMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XlsxSectionMode enum. Spécifie comment les sections sont gérées lors de l’enregistrement d’un document au format XLSX en C++."
type: docs
weight: 87000
url: /fr/cpp/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enum


Spécifie comment les sections sont gérées lors de l'enregistrement d'un document au format XLSX.

```cpp
enum class XlsxSectionMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| MultipleWorksheets | 0 | Spécifie qu’une feuille de calcul distincte est créée pour chaque section d’un document. |
| SingleWorksheet | 1 | Spécifie que toutes les sections d’un document sont enregistrées sur une seule feuille de calcul. |


## Exemples



Montre comment enregistrer le document en feuilles de calcul séparées.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Big document.docx");

// Chaque section d’un document sera créée en tant que feuille de calcul séparée.
// Utilisez 'SingleWorksheet' pour afficher tout le document sur une seule feuille de calcul.
auto xlsxSaveOptions = System::MakeObject<Aspose::Words::Saving::XlsxSaveOptions>();
xlsxSaveOptions->set_SectionMode(Aspose::Words::Saving::XlsxSectionMode::MultipleWorksheets);

doc->Save(get_ArtifactsDir() + u"XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

## Voir aussi

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
