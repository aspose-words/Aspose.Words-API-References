---
title: "Aspose::Words::Saving::MarkdownExportAsHtml enumeración"
linktitle: "MarkdownExportAsHtml"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownExportAsHtml enumeración. Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar en C++."
type: docs
weight: 66500
url: /es/cpp/aspose.words.saving/markdownexportashtml/
---
## MarkdownExportAsHtml enum


Permite especificar los elementos que se exportarán a Markdown como HTML sin procesar.

```cpp
enum class MarkdownExportAsHtml
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | 0 | Exporte todos los elementos usando la sintaxis Markdown sin ningún HTML sin procesar. |
| Tablas | 1 | Exportar tablas como HTML sin procesar. |
| NonCompatibleTables | 2 | Exportar tablas que no pueden representarse correctamente en Markdown puro como HTML sin procesar. |


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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
