---
title: "Aspose::Words::DocumentBuilder::InsertOnlineVideo método"
linktitle: "InsertOnlineVideo"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DocumentBuilder::InsertOnlineVideo método. Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado en C++."
type: docs
weight: 43000
url: /es/cpp/aspose.words/documentbuilder/insertonlinevideo/
---
## DocumentBuilder::InsertOnlineVideo(const System::String\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | const System::String\& | La URL del video. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

Se admite la inserción de video en línea desde los siguientes recursos:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Si su video en línea no se muestra correctamente, use [InsertOnlineVideo()](../), que acepta código HTML incrustado personalizado.

El código para incrustar video puede variar entre proveedores; consulte al proveedor correspondiente de su elección para obtener detalles.

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, Aspose::Words::Drawing::RelativeHorizontalPosition, double, Aspose::Words::Drawing::RelativeVerticalPosition, double, double, double, Aspose::Words::Drawing::WrapType) method


Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition horzPos, double left, Aspose::Words::Drawing::RelativeVerticalPosition vertPos, double top, double width, double height, Aspose::Words::Drawing::WrapType wrapType)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | const System::String\& | La URL del video. |
| videoEmbedCode | const System::String\& | El código de incrustación del video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Los bytes de la imagen en miniatura. |
| horzPos | Aspose::Words::Drawing::RelativeHorizontalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| left | double | Distancia en puntos desde el origen hasta el lado izquierdo de la imagen. |
| vertPos | Aspose::Words::Drawing::RelativeVerticalPosition | Especifica desde dónde se mide la distancia a la imagen. |
| top | double | Distancia en puntos desde el origen hasta el lado superior de la imagen. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| wrapType | Aspose::Words::Drawing::WrapType | Especifica cómo envolver el texto alrededor de la imagen. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar un video en línea en un documento con una miniatura personalizada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // A continuación se presentan dos formas de crear una forma con una miniatura personalizada, que enlaza a un video en línea
        // que se reproducirá cuando hagamos clic en la forma en Microsoft Word.
        // 1 -  Inserte una forma en línea en el cursor de inserción de nodo del constructor:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Inserte una forma flotante:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* Enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* Enum [WrapType](../../../aspose.words.drawing/wraptype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, const System::String\&, const System::ArrayPtr\<uint8_t\>\&, double, double) method


Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, const System::String &videoEmbedCode, const System::ArrayPtr<uint8_t> &thumbnailImageBytes, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | const System::String\& | La URL del video. |
| videoEmbedCode | const System::String\& | El código de incrustación del video. |
| thumbnailImageBytes | const System::ArrayPtr\<uint8_t\>\& | Los bytes de la imagen en miniatura. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

## Ejemplos



Muestra cómo insertar un video en línea en un documento con una miniatura personalizada.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String videoUrl = u"https://vimeo.com/52477838";
System::String videoEmbedCode = System::String(u"<iframe src=\"https://player.vimeo.com/video/52477838\" width=\"640\" height=\"360\" frameborder=\"0\" ") + u"title=\"Aspose\" webkitallowfullscreen mozallowfullscreen allowfullscreen></iframe>";

System::ArrayPtr<uint8_t> thumbnailImageBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");

{
    auto stream = System::MakeObject<System::IO::MemoryStream>(thumbnailImageBytes);
    {
        System::SharedPtr<System::Drawing::Image> image = System::Drawing::Image::FromStream(stream);
        // A continuación se presentan dos formas de crear una forma con una miniatura personalizada, que enlaza a un video en línea
        // que se reproducirá cuando hagamos clic en la forma en Microsoft Word.
        // 1 -  Inserte una forma en línea en el cursor de inserción de nodo del constructor:
        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, image->get_Width(), image->get_Height());

        builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

        // 2 -  Inserte una forma flotante:
        double left = builder->get_PageSetup()->get_RightMargin() - image->get_Width();
        double top = builder->get_PageSetup()->get_BottomMargin() - image->get_Height();

        builder->InsertOnlineVideo(videoUrl, videoEmbedCode, thumbnailImageBytes, Aspose::Words::Drawing::RelativeHorizontalPosition::RightMargin, left, Aspose::Words::Drawing::RelativeVerticalPosition::BottomMargin, top, image->get_Width(), image->get_Height(), Aspose::Words::Drawing::WrapType::Square);
    }
}

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertOnlineVideoCustomThumbnail.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertOnlineVideo(const System::String\&, double, double) method


Inserta un objeto de video en línea en el documento y lo escala al tamaño especificado.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Shape> Aspose::Words::DocumentBuilder::InsertOnlineVideo(const System::String &videoUrl, double width, double height)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| videoUrl | const System::String\& | La URL del video. |
| ancho | double | El ancho de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |
| alto | double | La altura de la imagen en puntos. Puede ser un valor negativo o cero para solicitar una escala del 100%. |

### ReturnValue

El nodo de imagen que acaba de insertarse.
## Observaciones


Puede cambiar el tamaño de la imagen, la ubicación, el método de posicionamiento y otras configuraciones usando el objeto [Shape](../../../aspose.words.drawing/shape/) devuelto por este método.

Se admite la inserción de video en línea desde los siguientes recursos:

* [https://www.youtube.com/](https://www.youtube.com/)
* [https://vimeo.com/](https://vimeo.com/)



Si su video en línea no se muestra correctamente, use [InsertOnlineVideo()](../), que acepta código HTML incrustado personalizado.

El código para incrustar video puede variar entre proveedores; consulte al proveedor correspondiente de su elección para obtener detalles.

## Ejemplos



Muestra cómo insertar un video en línea en un documento usando una URL.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertOnlineVideo(u"https://youtu.be/g1N9ke8Prmk", 360, 270);

// Podemos ver el video desde Microsoft Word haciendo clic en la forma.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertVideoWithUrl.docx");
```

## Ver también

* Class [Shape](../../../aspose.words.drawing/shape/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
