---
title: "Aspose::Words::Drawing::ImageData::Save método"
linktitle: "Save"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Drawing::ImageData::Save método. Guarda la imagen en el flujo especificado en C++."
type: docs
weight: 22000
url: /es/cpp/aspose.words.drawing/imagedata/save/
---
## ImageData::Save(const System::SharedPtr\<System::IO::Stream\>\&) method


Guarda la imagen en el flujo especificado.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| flujo | const System::SharedPtr\<System::IO::Stream\>\& | El flujo donde guardar la imagen. |
## Observaciones


¿Es responsabilidad del llamador eliminar el objeto de flujo?

## Ver también

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::Save(const System::String\&) method


Guarda la imagen en un archivo.

```cpp
void Aspose::Words::Drawing::ImageData::Save(const System::String &fileName)
```


| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| fileName | const System::String\& | El nombre de archivo donde guardar la imagen. |

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

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
## ImageData::Save(std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> void Aspose::Words::Drawing::ImageData::Save(std::basic_ostream<CharType, Traits> &stream)
```

## Ver también

* Class [ImageData](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
