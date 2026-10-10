---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting método"
linktitle: "get_ExportUnderlineFormatting"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting método. Obtiene o establece un valor booleano que indica si exportar el formato de subrayado del texto como una secuencia de dos caracteres más \"++\". El valor predeterminado es false en C++."
type: docs
weight: 3500
url: /es/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


Obtiene o establece un valor booleano que indica si exportar el formato de texto subrayado como una secuencia de dos caracteres más "++". El valor predeterminado es **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## Ejemplos



Muestra cómo exportar el formato de subrayado como ++.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## Ver también

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
