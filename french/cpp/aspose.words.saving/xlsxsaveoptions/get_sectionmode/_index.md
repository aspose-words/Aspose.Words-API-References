---
title: "Méthode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode"
linktitle: "get_SectionMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode method. Obtient ou définit la façon dont les sections sont gérées lors de l’enregistrement du document XLSX de sortie. La valeur par défaut est MultipleWorksheets en C++."
type: docs
weight: 4500
url: /fr/cpp/aspose.words.saving/xlsxsaveoptions/get_sectionmode/
---
## XlsxSaveOptions::get_SectionMode method


Obtient ou définit la façon dont les sections sont gérées lors de l’enregistrement du document XLSX de sortie. La valeur par défaut est [MultipleWorksheets](../../xlsxsectionmode/).

```cpp
Aspose::Words::Saving::XlsxSectionMode Aspose::Words::Saving::XlsxSaveOptions::get_SectionMode() const
```


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

* Enum [XlsxSectionMode](../../xlsxsectionmode/)
* Class [XlsxSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
