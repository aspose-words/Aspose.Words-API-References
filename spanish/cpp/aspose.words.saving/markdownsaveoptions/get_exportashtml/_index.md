---
title: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml"
linktitle: "get_ExportAsHtml"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml. Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar. El valor predeterminado es None en C++."
type: docs
weight: 2500
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_exportashtml/
---
## MarkdownSaveOptions::get_ExportAsHtml method


Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar. El valor predeterminado es [None](../../markdownexportashtml/).

```cpp
Aspose::Words::Saving::MarkdownExportAsHtml Aspose::Words::Saving::MarkdownSaveOptions::get_ExportAsHtml() const
```


## Ejemplos



Muestra cómo exportar una tabla a Markdown como HTML sin procesar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Sample table:");

// Crear tabla.
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Right);
builder->Write(u"Cell1");
builder->InsertCell();
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->Write(u"Cell2");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportAsHtml(Aspose::Words::Saving::MarkdownExportAsHtml::Tables);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportTableAsHtml.md", saveOptions);
```

## Ver también

* Enum [MarkdownExportAsHtml](../../markdownexportashtml/)
* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
