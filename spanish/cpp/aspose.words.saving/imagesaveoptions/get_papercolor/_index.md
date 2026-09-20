---
title: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor método"
linktitle: "get_PaperColor"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::ImageSaveOptions::get_PaperColor método. Obtiene o establece el color de fondo (papel) para las imágenes generadas. El valor predeterminado es Blanco en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.saving/imagesaveoptions/get_papercolor/
---
## ImageSaveOptions::get_PaperColor method


Obtiene o establece el color de fondo (papel) para las imágenes generadas. El valor predeterminado es **White**.

```cpp
System::Drawing::Color Aspose::Words::Saving::ImageSaveOptions::get_PaperColor()
```

## Observaciones


Al renderizar páginas de un documento que especifica su propio color de fondo, el color de fondo del documento sobrescribirá el color especificado por esta propiedad.

## Ejemplos



Renderiza una página de un documento Word en una imagen con fondo transparente o coloreado.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Name(u"Times New Roman");
builder->get_Font()->set_Size(24);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
// para modificar la forma en que ese método renderiza el documento en una imagen.
auto imgOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
// Establezca la propiedad "PaperColor" a un color transparente para aplicar un transparente
// fondo al documento mientras se renderiza a una imagen.
imgOptions->set_PaperColor(System::Drawing::Color::get_Transparent());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.Transparent.png", imgOptions);

// Establezca la propiedad "PaperColor" a un color opaco para aplicar ese color
// como fondo del documento al renderizarlo a una imagen.
imgOptions->set_PaperColor(System::Drawing::Color::get_LightCoral());

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.PaperColor.LightCoral.png", imgOptions);
```

## Ver también

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
