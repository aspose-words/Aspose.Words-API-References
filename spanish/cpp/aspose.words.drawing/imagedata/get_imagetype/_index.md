---
title: "Aspose::Words::Drawing::ImageData::get_ImageType método"
linktitle: "get_ImageType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageType método. Obtiene el tipo de la imagen en C++."
type: docs
weight: 15000
url: /es/cpp/aspose.words.drawing/imagedata/get_imagetype/
---
## ImageData::get_ImageType method


Obtiene el tipo de la imagen.

```cpp
Aspose::Words::Drawing::ImageType Aspose::Words::Drawing::ImageData::get_ImageType()
```


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

## Ver también

* Enum [ImageType](../../imagetype/)
* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
