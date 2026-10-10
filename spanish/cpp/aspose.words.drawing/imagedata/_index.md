---
title: "Aspose::Words::Drawing::ImageData class"
linktitle: "ImageData"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData class. Define una imagen para una forma. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 6000
url: /es/cpp/aspose.words.drawing/imagedata/
---
## ImageData class


Define una imagen para una forma. Para obtener más información, visite el artículo de documentación [Working with Images](https://docs.aspose.com/words/cpp/working-with-images/).

```cpp
class ImageData : public Aspose::Words::IBorderAttrSource
```

## Métodos

| Método | Descripción |
| --- | --- |
| [FitImageToShape](./fitimagetoshape/)() | Ajusta los datos de imagen al marco de [Shape](../shape/) para que la relación de aspecto de los datos de imagen coincida con la relación de aspecto del marco de [Shape](../shape/). |
| [get_BiLevel](./get_bilevel/)() | Determina si una imagen se mostrará en blanco y negro. |
| [get_Borders](./get_borders/)() | Obtiene la colección de bordes de la imagen. Los bordes solo tienen efecto en imágenes en línea. |
| [get_Brightness](./get_brightness/)() | Obtiene o establece el brillo de la imagen. El valor de esta propiedad debe ser un número entre 0.0 (más oscuro) y 1.0 (más brillante). |
| [get_ChromaKey](./get_chromakey/)() | Define el valor de color de la imagen que se tratará como transparente. |
| [get_Contrast](./get_contrast/)() | Obtiene o establece el contraste de la imagen especificada. El valor de esta propiedad debe ser un número entre 0.0 (menor contraste) y 1.0 (mayor contraste). |
| [get_CropBottom](./get_cropbottom/)() | Define la fracción de recorte de la imagen desde el lado inferior. |
| [get_CropLeft](./get_cropleft/)() | Define la fracción de recorte de la imagen desde el lado izquierdo. |
| [get_CropRight](./get_cropright/)() | Define la fracción de recorte de la imagen desde el lado derecho. |
| [get_CropTop](./get_croptop/)() | Define la fracción de recorte de la imagen desde el lado superior. |
| [get_GrayScale](./get_grayscale/)() | Determina si una imagen se mostrará en modo escala de grises. |
| [get_HasImage](./get_hasimage/)() | Devuelve **true** si la forma tiene bytes de imagen o enlaza una imagen. |
| [get_ImageBytes](./get_imagebytes/)() | Obtiene o establece los bytes sin procesar de la imagen almacenada en la forma. |
| [get_ImageSize](./get_imagesize/)() | Obtiene la información sobre el tamaño y la resolución de la imagen. |
| [get_ImageType](./get_imagetype/)() | Obtiene el tipo de la imagen. |
| [get_IsLink](./get_islink/)() | Devuelve **true** si la imagen está vinculada a la forma (cuando se especifica [SourceFullName](./get_sourcefullname/)). |
| [get_IsLinkOnly](./get_islinkonly/)() | Devuelve **true** si la imagen está vinculada y no está almacenada en el documento. |
| [get_SourceFullName](./get_sourcefullname/)() | Obtiene o establece la ruta y el nombre del archivo fuente para la imagen vinculada. |
| [get_Title](./get_title/)() | Define el título de una imagen. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Save](./save/)(const System::SharedPtr\<System::IO::Stream\>\&) | Guarda la imagen en el flujo especificado. |
| [Save](./save/)(const System::String\&) | Guarda la imagen en un archivo. |
| [Save](./save/)(std::basic_ostream\<CharType, Traits\>\&) |  |
| [set_BiLevel](./set_bilevel/)(bool) | Método set para [Aspose::Words::Drawing::ImageData::get_BiLevel](./get_bilevel/). |
| [set_Brightness](./set_brightness/)(double) | Método set para [Aspose::Words::Drawing::ImageData::get_Brightness](./get_brightness/). |
| [set_ChromaKey](./set_chromakey/)(System::Drawing::Color) | Método set para [Aspose::Words::Drawing::ImageData::get_ChromaKey](./get_chromakey/). |
| [set_Contrast](./set_contrast/)(double) | Método set para [Aspose::Words::Drawing::ImageData::get_Contrast](./get_contrast/). |
| [set_CropBottom](./set_cropbottom/)(double) | Método set para [Aspose::Words::Drawing::ImageData::get_CropBottom](./get_cropbottom/). |
| [set_CropLeft](./set_cropleft/)(double) | Método set para [Aspose::Words::Drawing::ImageData::get_CropLeft](./get_cropleft/). |
| [set_CropRight](./set_cropright/)(double) | Método set para [Aspose::Words::Drawing::ImageData::get_CropRight](./get_cropright/). |
| [set_CropTop](./set_croptop/)(double) | Método set para [Aspose::Words::Drawing::ImageData::get_CropTop](./get_croptop/). |
| [set_GrayScale](./set_grayscale/)(bool) | Método set para [Aspose::Words::Drawing::ImageData::get_GrayScale](./get_grayscale/). |
| [set_ImageBytes](./set_imagebytes/)(const System::ArrayPtr\<uint8_t\>\&) | Método set para [Aspose::Words::Drawing::ImageData::get_ImageBytes](./get_imagebytes/). |
| [set_SourceFullName](./set_sourcefullname/)(const System::String\&) | Método set para [Aspose::Words::Drawing::ImageData::get_SourceFullName](./get_sourcefullname/). |
| [set_Title](./set_title/)(const System::String\&) | Método set para [Aspose::Words::Drawing::ImageData::get_Title](./get_title/). |
| [SetImage](./setimage/)(const System::SharedPtr\<System::Drawing::Image\>\&) | Establece la imagen que muestra la forma. |
| [SetImage](./setimage/)(const System::SharedPtr\<System::IO::Stream\>\&) | Establece la imagen que muestra la forma. |
| [SetImage](./setimage/)(const System::String\&) | Establece la imagen que muestra la forma. |
| [SetImage](./setimage/)(std::basic_istream\<CharType, Traits\>\&) |  |
| [ToByteArray](./tobytearray/)() | Devuelve los bytes de la imagen para cualquier imagen, independientemente de si la imagen está almacenada o vinculada. |
| [ToImage](./toimage/)() | Obtiene la imagen almacenada en la forma como un objeto **Image**. |
| [ToStream](./tostream/)() | Crea y devuelve un flujo que contiene los bytes de la imagen. |
| static [Type](./type/)() |  |
## Observaciones


Utilice la propiedad [ImageData](../shape/get_imagedata/) para acceder y modificar la imagen dentro de una forma. No crea instancias de la clase [ImageData](./) directamente.

Una imagen puede almacenarse dentro de una forma, enlazarse a un archivo externo o ambas (enlazada y almacenada en el documento).

Independientemente de si la imagen está almacenada dentro de la forma o enlazada, siempre puede acceder a la imagen real utilizando los métodos [ToByteArray](./tobytearray/), [ToStream](./tostream/), [ToImage](./toimage/) o [Save()](../). Si la imagen está almacenada dentro de la forma, también puede acceder a ella directamente mediante la propiedad [ImageBytes](./get_imagebytes/).

Para almacenar una imagen dentro de una forma, use el método [SetImage()](../). Para enlazar una imagen a una forma, establezca la propiedad [SourceFullName](./get_sourcefullname/).

## Ejemplos



Muestra cómo extraer imágenes de un documento y guardarlas en el sistema de archivos local como archivos individuales.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

// Obtenga la colección de formas del documento,
// y guarde los datos de imagen de cada forma que contenga una imagen como un archivo en el sistema de archivos local.
System::SharedPtr<Aspose::Words::NodeCollection> shapes = doc->GetChildNodes(Aspose::Words::NodeType::Shape, true);

ASSERT_EQ(9, shapes->LINQ_Count(static_cast<System::Func<System::SharedPtr<Aspose::Words::Node>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::Node> s)>>([](System::SharedPtr<Aspose::Words::Node> s) -> bool
{
    return (System::ExplicitCast<Aspose::Words::Drawing::Shape>(s))->get_HasImage();
}))));

int32_t imageIndex = 0;
for (auto&& shape : System::IterateOver(shapes->LINQ_OfType<System::SharedPtr<Aspose::Words::Drawing::Shape> >()))
{
    if (shape->get_HasImage())
    {
        // Los datos de imagen de las formas pueden contener imágenes de muchos formatos posibles.
        // Podemos determinar automáticamente una extensión de archivo para cada imagen, basándonos en su formato.
        System::String imageFileName = System::String::Format(u"File.ExtractImages.{0}{1}", imageIndex, Aspose::Words::FileFormatUtil::ImageTypeToExtension(shape->get_ImageData()->get_ImageType()));
        shape->get_ImageData()->Save(get_ArtifactsDir() + imageFileName);
        imageIndex++;
    }
}
```


Muestra cómo insertar una imagen enlazada en un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::String imageFileName = get_ImageDir() + u"Windows MetaFile.wmf";

// A continuación se presentan dos formas de aplicar una imagen a una forma para que pueda mostrarla.
// 1 -  Configure la forma para que contenga la imagen.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->SetImage(imageFileName);

builder->InsertNode(shape);

doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx");

// Cada imagen que almacenemos en la forma aumentará el tamaño de nuestro documento.
ASSERT_TRUE(70000 < System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Embedded.docx")->get_Length());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->RemoveAllChildren();

// 2 -  Configure la forma para enlazar a un archivo de imagen en el sistema de archivos local.
shape = System::MakeObject<Aspose::Words::Drawing::Shape>(builder->get_Document(), Aspose::Words::Drawing::ShapeType::Image);
shape->set_WrapType(Aspose::Words::Drawing::WrapType::Inline);
shape->get_ImageData()->set_SourceFullName(imageFileName);

builder->InsertNode(shape);
doc->Save(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx");

// Enlazar imágenes ahorrará espacio y resultará en un documento más pequeño.
// Sin embargo, el documento solo puede mostrar la imagen correctamente mientras
// el archivo de imagen está presente en la ubicación a la que apunta la propiedad "SourceFullName" de la forma.
ASSERT_TRUE(10000 > System::MakeObject<System::IO::FileInfo>(get_ArtifactsDir() + u"Image.CreateLinkedImage.Linked.docx")->get_Length());
```

## Ver también

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
