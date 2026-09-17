---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode méthode"
linktitle: "get_OfficeMathExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode méthode. Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut est Text en C++."
type: docs
weight: 6500
url: /fr/cpp/aspose.words.saving/markdownsaveoptions/get_officemathexportmode/
---
## MarkdownSaveOptions::get_OfficeMathExportMode method


Spécifie comment OfficeMath sera écrit dans le fichier de sortie. La valeur par défaut est [Text](../../markdownofficemathexportmode/).

```cpp
Aspose::Words::Saving::MarkdownOfficeMathExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode() const
```


## Exemples



Montre comment OfficeMath sera écrit dans le document.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Montre comment exporter l'objet OfficeMath en LaTeX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


Montre comment exporter l'objet OfficeMath en MarkItDown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## Voir aussi

* Enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
