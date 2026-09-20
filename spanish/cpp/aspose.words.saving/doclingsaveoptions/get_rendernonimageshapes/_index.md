---
title: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes método"
linktitle: "get_RenderNonImageShapes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes método. Obtiene o establece un valor que indica si las formas que no son imágenes deben renderizarse y escribirse en el documento JSON de salida Docling en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


Obtiene o establece un valor que indica si las formas que no son imágenes deben renderizarse y escribirse en el documento JSON de salida Docling.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
```


## Ejemplos



Muestra cómo guardar un documento en formato JSON Docling.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// Establezca en true para renderizar las formas que no son imágenes e incluirlas en la salida.
// Establezca en false (por defecto) para excluir las formas que no son imágenes de la salida.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## Ver también

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
