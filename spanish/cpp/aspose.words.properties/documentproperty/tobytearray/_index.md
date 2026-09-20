---
title: "Método Aspose::Words::Properties::DocumentProperty::ToByteArray"
linktitle: "ToByteArray"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Properties::DocumentProperty::ToByteArray. Devuelve el valor de la propiedad como una matriz de bytes en C++."
type: docs
weight: 11000
url: /es/cpp/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty::ToByteArray method


Devuelve el valor de la propiedad como matriz de bytes.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::DocumentProperty::ToByteArray()
```

## Observaciones


Lanza una excepción si el tipo de la propiedad no es [ByteArray](../../propertytype/).

## Ejemplos



Muestra cómo agregar una miniatura a un documento que guardamos como Epub.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// If we save a document, whose "Thumbnail" property contains image data that we added, as an Epub,
// un lector que abra ese documento puede mostrar la imagen antes de la primera página.
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> properties = doc->get_BuiltInDocumentProperties();

System::ArrayPtr<uint8_t> thumbnailBytes = System::IO::File::ReadAllBytes(get_ImageDir() + u"Logo.jpg");
properties->set_Thumbnail(thumbnailBytes);

doc->Save(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.epub");

// Podemos extraer la imagen de miniatura de un documento y guardarla en el sistema de archivos local.
System::SharedPtr<Aspose::Words::Properties::DocumentProperty> thumbnail = doc->get_BuiltInDocumentProperties()->idx_get(u"Thumbnail");
System::IO::File::WriteAllBytes(get_ArtifactsDir() + u"DocumentProperties.Thumbnail.gif", thumbnail->ToByteArray());
```

## Ver también

* Class [DocumentProperty](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
