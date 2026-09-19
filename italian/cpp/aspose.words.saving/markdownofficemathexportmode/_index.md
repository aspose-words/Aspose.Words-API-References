---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum. Specifica come Aspose.Words esporta OfficeMath in Markdown in C++."
type: docs
weight: 68500
url: /it/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Specifica come Aspose.Words esporta OfficeMath in Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Testo | 0 | Esporta OfficeMath come testo semplice. |
| Immagine | 1 | Esporta OfficeMath come immagine. |
| MathML | 2 | Esporta OfficeMath come MathML. |
| Latex | 3 | Esporta OfficeMath come LaTeX. |
| MarkItDown | 4 | Esporta OfficeMath come LaTeX compatibile con MarkItDown. |


## Esempi



Mostra come OfficeMath verrà scritto nel documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Mostra come esportare l'oggetto OfficeMath come LaTeX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


Mostra come esportare l'oggetto OfficeMath come MarkItDown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## Vedi anche

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
