---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode énumération"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode énumération. Spécifie comment Aspose.Words exporte OfficeMath vers Markdown en C++."
type: docs
weight: 68500
url: /fr/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Spécifie comment Aspose.Words exporte OfficeMath vers Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| Texte | 0 | Exportez OfficeMath en texte brut. |
| Image | 1 | Exporter OfficeMath en tant qu'image. |
| MathML | 2 | Exporter OfficeMath en tant que MathML. |
| Latex | 3 | Exportez OfficeMath en LaTeX. |
| MarkItDown | 4 | Exporter OfficeMath en LaTeX compatible avec MarkItDown. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
