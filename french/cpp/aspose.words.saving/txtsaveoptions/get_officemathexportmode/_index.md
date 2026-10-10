---
title: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode méthode"
linktitle: "get_OfficeMathExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode méthode. Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut est Text en C++."
type: docs
weight: 5500
url: /fr/cpp/aspose.words.saving/txtsaveoptions/get_officemathexportmode/
---
## TxtSaveOptions::get_OfficeMathExportMode method


Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut est [Text](../../txtofficemathexportmode/).

```cpp
Aspose::Words::Saving::TxtOfficeMathExportMode Aspose::Words::Saving::TxtSaveOptions::get_OfficeMathExportMode() const
```


## Exemples



Montre comment exporter l'objet OfficeMath en Latex dans un fichier TXT.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::TxtOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.ExportOfficeMathAsLatexToText.txt", saveOptions);
```

## Voir aussi

* Enum [TxtOfficeMathExportMode](../../txtofficemathexportmode/)
* Class [TxtSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
