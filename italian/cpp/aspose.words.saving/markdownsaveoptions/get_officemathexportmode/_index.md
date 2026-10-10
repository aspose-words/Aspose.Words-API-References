---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode metodo"
linktitle: "get_OfficeMathExportMode"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode metodo. Specifica come OfficeMath verrà scritto nel file di output. Il valore predefinito è Text in C++."
type: docs
weight: 6500
url: /it/cpp/aspose.words.saving/markdownsaveoptions/get_officemathexportmode/
---
## MarkdownSaveOptions::get_OfficeMathExportMode method


Specifica come OfficeMath verrà scritto nel file di output. Il valore predefinito è [Text](../../markdownofficemathexportmode/).

```cpp
Aspose::Words::Saving::MarkdownOfficeMathExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode() const
```


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

* Enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
