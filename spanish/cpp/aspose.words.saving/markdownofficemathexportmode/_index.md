---
title: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum"
linktitle: "MarkdownOfficeMathExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownOfficeMathExportMode enum. Especifica cómo Aspose.Words exporta OfficeMath a Markdown en C++."
type: docs
weight: 68500
url: /es/cpp/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enum


Especifica cómo Aspose.Words exporta OfficeMath a Markdown.

```cpp
enum class MarkdownOfficeMathExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Text | 0 | Exporta OfficeMath como texto plano. |
| Image | 1 | Exportar OfficeMath como imagen. |
| MathML | 2 | Exportar OfficeMath como MathML. |
| Latex | 3 | Exporta OfficeMath como LaTeX. |
| MarkItDown | 4 | Exportar OfficeMath como LaTeX que sea compatible con MarkItDown. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
