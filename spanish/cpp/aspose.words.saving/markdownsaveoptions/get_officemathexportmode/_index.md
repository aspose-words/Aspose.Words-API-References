---
title: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode"
linktitle: "get_OfficeMathExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode método. Especifica cómo se escribirá OfficeMath en el archivo de salida. El valor predeterminado es Text en C++."
type: docs
weight: 6500
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_officemathexportmode/
---
## MarkdownSaveOptions::get_OfficeMathExportMode method


Especifica cómo se escribirá OfficeMath en el archivo de salida. El valor predeterminado es [Text](../../markdownofficemathexportmode/).

```cpp
Aspose::Words::Saving::MarkdownOfficeMathExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_OfficeMathExportMode() const
```


## Ejemplos



Muestra cómo se escribirá OfficeMath en el documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Image);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```


Muestra cómo exportar el objeto OfficeMath como LaTeX.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::Latex);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsLatex.md", saveOptions);
```


Muestra cómo exportar el objeto OfficeMath como MarkItDown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_OfficeMathExportMode(Aspose::Words::Saving::MarkdownOfficeMathExportMode::MarkItDown);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportOfficeMathAsMarkItDown.md", saveOptions);
```

## Ver también

* Enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
