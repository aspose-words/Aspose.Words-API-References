---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum. Anger hur Aspose.Words exporterar OfficeMath till Markdown i C++."
type: docs
weight: 68500
url: /sv/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Anger hur Aspose.Words exporterar OfficeMath till Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Text | 0 | Exportera OfficeMath som vanlig text. |
| Image | 1 | Exportera OfficeMath som bild. |
| MathML | 2 | Exportera OfficeMath som MathML. |
| Latex | 3 | Exportera OfficeMath som LaTeX. |
| MarkItDown | 4 | Exportera OfficeMath som LaTeX som är kompatibel med MarkItDown. |


## Exempel



Visar hur OfficeMath kommer att skrivas till dokumentet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Visar hur man exporterar OfficeMath-objektet som Latex.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


Visar hur man exporterar OfficeMath-objektet som MarkItDown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## Se även

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
