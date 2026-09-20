---
title: "Aspose::Words::Drawing::ImageData::get_ImageBytes método"
linktitle: "get_ImageBytes"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::get_ImageBytes método. Obtiene o establece los bytes sin procesar de la imagen almacenada en la forma en C++."
type: docs
weight: 13000
url: /es/cpp/aspose.words.drawing/imagedata/get_imagebytes/
---
## ImageData::get_ImageBytes method


Obtiene o establece los bytes sin procesar de la imagen almacenada en la forma.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Drawing::ImageData::get_ImageBytes()
```

## Observaciones


Establecer el valor a **null** o a una matriz vacía eliminará la imagen de la forma.

Devuelve **null** si la imagen no está almacenada en el documento (p. ej., la imagen probablemente está vinculada en este caso).

## Ejemplos



Muestra cómo crear un archivo de imagen a partir de los datos de imagen sin procesar de una forma.
```cpp
auto imgSourceDoc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto imgShape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(imgSourceDoc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_TRUE(imgShape->get_HasImage());

// ToByteArray() devuelve el arreglo almacenado en la propiedad ImageBytes.
ASPOSE_ASSERT_EQ(imgShape->get_ImageData()->get_ImageBytes(), imgShape->get_ImageData()->ToByteArray());

// Guarde los datos de imagen de la forma en un archivo de imagen en el sistema de archivos local.
{
    System::SharedPtr<System::IO::Stream> imgStream = imgShape->get_ImageData()->ToStream();
    {
        auto outStream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"Drawing.GetDataFromImage.png", System::IO::FileMode::Create, System::IO::FileAccess::ReadWrite);
        imgStream->CopyTo(outStream);
    }
}
```

## Ver también

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
