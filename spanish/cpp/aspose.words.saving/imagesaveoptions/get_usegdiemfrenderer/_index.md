---
title: "Método Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer"
linktitle: "get_UseGdiEmfRenderer"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer. Obtiene o establece un valor que determina si se usa el renderizador de metarchivo GDI+ o el de Aspose.Words al guardar en EMF en C++."
type: docs
weight: 18000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_usegdiemfrenderer/
---
## ImageSaveOptions::get_UseGdiEmfRenderer method


Obtiene o establece un valor que determina si se usa GDI+ o Aspose.Words metafile renderer al guardar en EMF.

```cpp
bool Aspose::Words::Saving::ImageSaveOptions::get_UseGdiEmfRenderer() const
```

## Observaciones


Si se establece en **true**, se usa el renderizador de metarchivo GDI+. Es decir, el contenido se escribe en un objeto gráfico GDI+ y se guarda en el metarchivo.

Si se establece en **false**, se usa el renderizador de metarchivo de Aspose.Words. Es decir, el contenido se escribe directamente en el formato de metarchivo con Aspose.Words.

Tiene efecto solo al guardar en EMF.

El guardado con GDI+ funciona solo en .NET.

El valor predeterminado es **true**.

## Ejemplos



Muestra cómo elegir un renderizador al convertir un documento a .emf.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cuando guardamos el documento como una imagen EMF, podemos pasar un objeto SaveOptions para seleccionar un renderizador para la imagen.
// Si establecemos la bandera "UseGdiEmfRenderer" a "true", Aspose.Words usará el renderizador GDI+.
// Si establecemos la bandera "UseGdiEmfRenderer" a "false", Aspose.Words usará su propio renderizador de metarchivos.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Emf);
saveOptions->set_UseGdiEmfRenderer(useGdiEmfRenderer);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.Renderer.emf", saveOptions);
```

## Ver también

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
