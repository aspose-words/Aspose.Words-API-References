---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode método"
linktitle: "get_ListExportMode"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode método. Especifica cómo se escribirán los elementos de la lista en el archivo de salida. El valor predeterminado es MarkdownSyntax en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_listexportmode/
---
## MarkdownSaveOptions::get_ListExportMode method


Especifica cómo se escribirán los elementos de la lista en el archivo de salida. El valor predeterminado es [MarkdownSyntax](../../markdownlistexportmode/).

```cpp
Aspose::Words::Saving::MarkdownListExportMode Aspose::Words::Saving::MarkdownSaveOptions::get_ListExportMode() const
```

## Observaciones


Cuando esta propiedad se establece en [PlainText](../../markdownlistexportmode/) todas las etiquetas de la lista se actualizan mediante [UpdateListLabels](../../../aspose.words/document/updatelistlabels/) y se exportan con sus valores reales. Tales listas pueden no ser compatibles con el formato Markdown y serán reconocidas como texto plano al importarlas en este caso.

Cuando esta propiedad se establece en [MarkdownSyntax](../../markdownlistexportmode/), el escritor intenta exportar los elementos de la lista de manera que permita numerar los elementos automáticamente mediante Markdown.

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

* Enum [MarkdownListExportMode](../../markdownlistexportmode/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
