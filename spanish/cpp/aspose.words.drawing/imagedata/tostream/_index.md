---
title: "Aspose::Words::Drawing::ImageData::ToStream método"
linktitle: "ToStream"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::ToStream método. Crea y devuelve un flujo que contiene los bytes de la imagen en C++."
type: docs
weight: 38000
url: /es/cpp/aspose.words.drawing/imagedata/tostream/
---
## ImageData::ToStream method


Crea y devuelve un flujo que contiene los bytes de la imagen.

```cpp
System::SharedPtr<System::IO::Stream> Aspose::Words::Drawing::ImageData::ToStream()
```

## Observaciones


Si los bytes de la imagen están almacenados en la forma, crea y devuelve un objeto **MemoryStream**.

Si la imagen está vinculada y almacenada en un archivo, abre el archivo y devuelve un objeto **FileStream**.

Si la imagen está vinculada y almacenada en una URL externa, descarga el archivo y devuelve un objeto **MemoryStream**.

¿Es responsabilidad del llamador eliminar el objeto de flujo?

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
