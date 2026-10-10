---
title: "Método Aspose::Words::Saving::PclSaveOptions::AddPrinterFont"
linktitle: "AddPrinterFont"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::PclSaveOptions::AddPrinterFont. Añade información sobre la fuente que el fabricante carga en la impresora en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/pclsaveoptions/addprinterfont/
---
## PclSaveOptions::AddPrinterFont method


Agrega información sobre la fuente que el fabricante sube a la impresora.

```cpp
void Aspose::Words::Saving::PclSaveOptions::AddPrinterFont(const System::String &fontFullName, const System::String &fontPclName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fontFullName | const System::String\& | Nombre completo de la fuente (p. ej. "Times New Roman Bold Italic"). |
| fontPclName | const System::String\& | Nombre de la fuente que se usa en el documento Pcl. |

## Ejemplos



Muestra cómo hacer que una impresora sustituya todas las instancias de una fuente específica por otra fuente diferente.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Courier");
builder->Write(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::PclSaveOptions>();
saveOptions->AddPrinterFont(u"Courier New", u"Courier");

// Al imprimir este documento, la impresora usará la fuente "Courier New"
// para acceder a los lugares donde nuestro documento usó la fuente "Courier".
doc->Save(get_ArtifactsDir() + u"PclSaveOptions.AddPrinterFont.pcl", saveOptions);
```

## Ver también

* Class [PclSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
