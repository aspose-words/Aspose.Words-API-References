---
title: "Método Aspose::Words::FileFormatUtil::ImageTypeToExtension"
linktitle: "ImageTypeToExtension"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::FileFormatUtil::ImageTypeToExtension. Convierte un valor enumerado de tipo de imagen de Aspose.Words en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/fileformatutil/imagetypetoextension/
---
## FileFormatUtil::ImageTypeToExtension method


Convierte un valor enumerado de tipo de imagen de Aspose.Words en una extensión de archivo. La extensión devuelta es una cadena en minúsculas con un punto inicial.

```cpp
static System::String Aspose::Words::FileFormatUtil::ImageTypeToExtension(Aspose::Words::Drawing::ImageType imageType)
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

* Enum [ImageType](../../../aspose.words.drawing/imagetype/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
