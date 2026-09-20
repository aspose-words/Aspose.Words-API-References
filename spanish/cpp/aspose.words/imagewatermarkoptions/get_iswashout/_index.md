---
title: "Aspose::Words::ImageWatermarkOptions::get_IsWashout método"
linktitle: "get_IsWashout"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ImageWatermarkOptions::get_IsWashout método. Obtiene o establece un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. El valor predeterminado es true en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/imagewatermarkoptions/get_iswashout/
---
## ImageWatermarkOptions::get_IsWashout method


Obtiene o establece un valor booleano que es responsable del efecto de desvanecimiento de la marca de agua. El valor predeterminado es **true**.

```cpp
bool Aspose::Words::ImageWatermarkOptions::get_IsWashout() const
```


## Ejemplos



Muestra cómo crear una marca de agua a partir de una imagen en el sistema de archivos local.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifique la apariencia de la marca de agua de imagen con un objeto ImageWatermarkOptions,
// luego páselo al crear una marca de agua a partir de un archivo de imagen.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);
imageWatermarkOptions->set_IsWashout(false);

// Tenemos diferentes opciones para insertar una imagen.
// Utilice uno de los siguientes métodos para agregar una marca de agua de imagen.
doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"));

doc->get_Watermark()->SetImage(System::Drawing::Image::FromFile(get_ImageDir() + u"Logo.jpg"), imageWatermarkOptions);

doc->get_Watermark()->SetImage(get_ImageDir() + u"Logo.jpg", imageWatermarkOptions);

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermark.docx");
```

## Ver también

* Class [ImageWatermarkOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
