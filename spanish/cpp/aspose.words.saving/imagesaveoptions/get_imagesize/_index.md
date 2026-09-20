---
title: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize método"
linktitle: "get_ImageSize"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_ImageSize método. Obtiene o establece el tamaño de una imagen generada en píxeles en C++."
type: docs
weight: 7500
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_imagesize/
---
## ImageSaveOptions::get_ImageSize method


Obtiene o establece el tamaño de una imagen generada en píxeles.

```cpp
System::Drawing::Size Aspose::Words::Saving::ImageSaveOptions::get_ImageSize() const
```

## Observaciones


Esta propiedad tiene efecto solo al guardar en formatos de imagen raster.

El valor predeterminado es (0 x 0), lo que significa que el tamaño de la imagen generada se calculará según el tamaño de la imagen en puntos, la resolución especificada y la escala.

## Ejemplos



Muestra cómo renderizar cada página de un documento a una imagen TIFF separada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Page 1.");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 2.");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->Writeln(u"Page 3.");

// Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
// para modificar la forma en que ese método renderiza el documento en una imagen.
auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Tiff);

for (int32_t i = 0; i < doc->get_PageCount(); i++)
{
    // Establezca la propiedad "PageSet" al número de la primera página desde
    // desde la cual comenzar a renderizar el documento.
    options->set_PageSet(System::MakeObject<Aspose::Words::Saving::PageSet>(i));
    // Exportar página a 2325x5325 píxeles y 600 ppp.
    options->set_Resolution(600.0f);
    options->set_ImageSize(System::Drawing::Size(2325, 5325));

    doc->Save(get_ArtifactsDir() + System::String::Format(u"ImageSaveOptions.PageByPage.{0}.tiff", i + 1), options);
}
```

## Ver también

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
