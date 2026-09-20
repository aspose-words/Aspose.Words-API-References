---
title: "Aspose::Words::ImageWatermarkOptions::get_Scale método"
linktitle: "get_Scale"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::ImageWatermarkOptions::get_Scale método. Obtiene o establece el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0 - auto en C++."
type: docs
weight: 4000
url: /es/cpp/aspose.words/imagewatermarkoptions/get_scale/
---
## ImageWatermarkOptions::get_Scale method


Obtiene o establece el factor de escala expresado como una fracción de la imagen. El valor predeterminado es 0 - automático.

```cpp
double Aspose::Words::ImageWatermarkOptions::get_Scale() const
```

## Observaciones


Los valores válidos van de 0 a 65,5 inclusive.

La escala automática significa que la marca de agua se escalará a su ancho máximo y altura máxima en relación con los márgenes de la página.

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
