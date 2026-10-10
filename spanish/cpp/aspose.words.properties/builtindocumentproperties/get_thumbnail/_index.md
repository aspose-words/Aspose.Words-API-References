---
title: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail método"
linktitle: "get_Thumbnail"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail método. Obtiene o establece la miniatura del documento en C++."
type: docs
weight: 28000
url: /es/cpp/aspose.words.properties/builtindocumentproperties/get_thumbnail/
---
## BuiltInDocumentProperties::get_Thumbnail method


Obtiene o establece la miniatura del documento.

```cpp
System::ArrayPtr<uint8_t> Aspose::Words::Properties::BuiltInDocumentProperties::get_Thumbnail()
```

## Observaciones


Por ahora, esta propiedad se usa solo cuando un documento se exporta a ePub; no se lee ni escribe en otros formatos de documento.

Se puede establecer una imagen de formato arbitrario en esta propiedad, pero el formato se verifica durante la exportación.

Solo se pueden usar imágenes gif, jpeg y png para la publicación ePub.

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

* Class [BuiltInDocumentProperties](../)
* Namespace [Aspose::Words::Properties](../../)
* Library [Aspose.Words for C++](../../../)
