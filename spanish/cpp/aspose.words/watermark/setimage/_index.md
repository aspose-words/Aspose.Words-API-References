---
title: "Método Aspose::Words::Watermark::SetImage"
linktitle: "SetImage"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Watermark::SetImage. Añade una marca de agua de imagen al documento en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words/watermark/setimage/
---
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&) method


Agrega una marca de agua de imagen al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Imagen que se muestra como marca de agua. |

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

* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::Drawing::Image\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::Drawing::Image> &image, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| image | const System::SharedPtr\<System::Drawing::Image\>\& | Imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |

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

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::SharedPtr<System::IO::Stream> &imageStream, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageStream | const System::SharedPtr\<System::IO::Stream\>\& | El flujo que contiene los datos de la imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |

## Ejemplos



Muestra cómo crear una marca de agua a partir de un flujo de imagen.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Modifique la apariencia de la marca de agua de imagen con un objeto ImageWatermarkOptions,
// luego páselo al crear una marca de agua a partir de un archivo de imagen.
auto imageWatermarkOptions = System::MakeObject<Aspose::Words::ImageWatermarkOptions>();
imageWatermarkOptions->set_Scale(5);

{
    auto imageStream = System::MakeObject<System::IO::FileStream>(get_ImageDir() + u"Logo.jpg", System::IO::FileMode::Open, System::IO::FileAccess::Read);
    doc->get_Watermark()->SetImage(imageStream, imageWatermarkOptions);
}

doc->Save(get_ArtifactsDir() + u"Document.ImageWatermarkStream.docx");
```

## Ver también

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## Watermark::SetImage(const System::String\&, const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\&) method


Agrega una marca de agua de imagen al documento.

```cpp
void Aspose::Words::Watermark::SetImage(const System::String &imagePath, const System::SharedPtr<Aspose::Words::ImageWatermarkOptions> &options)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imagePath | const System::String\& | Ruta al archivo de imagen que se muestra como marca de agua. |
| opciones | const System::SharedPtr\<Aspose::Words::ImageWatermarkOptions\>\& | Define opciones adicionales para la marca de agua de imagen. |

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

* Class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* Class [Watermark](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
