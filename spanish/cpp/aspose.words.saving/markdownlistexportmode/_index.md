---
title: "Aspose::Words::Saving::MarkdownListExportMode enumeración"
linktitle: "MarkdownListExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownListExportMode enumeración. Especifica cómo se exportan las listas a Markdown en C++."
type: docs
weight: 68000
url: /es/cpp/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enum


Especifica cómo se exportan las listas a Markdown.

```cpp
enum class MarkdownListExportMode
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| MarkdownSyntax | 0 | Exporta los elementos de la lista compatibles con la sintaxis Markdown. |
| PlainText | 1 | Exportar los elementos de la lista como texto sin formato. |


## Ejemplos



Muestra cómo se escribirán los elementos de la lista en el documento markdown.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"List item.docx");

// Utilice MarkdownListExportMode.PlainText o MarkdownListExportMode.MarkdownSyntax para exportar la lista.
auto options = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
options->set_ListExportMode(markdownListExportMode);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ListExportMode.md", options);
```

## Ver también

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
