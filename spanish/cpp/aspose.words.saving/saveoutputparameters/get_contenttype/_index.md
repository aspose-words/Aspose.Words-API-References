---
title: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType método"
linktitle: "get_ContentType"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Saving::SaveOutputParameters::get_ContentType método. Devuelve la cadena Content-Type (Tipo de medio de Internet) que identifica el tipo del documento guardado en C++."
type: docs
weight: 2000
url: /es/cpp/aspose.words.saving/saveoutputparameters/get_contenttype/
---
## SaveOutputParameters::get_ContentType method


Devuelve la cadena Content-Type (Tipo de medio de Internet) que identifica el tipo del documento guardado.

```cpp
System::String Aspose::Words::Saving::SaveOutputParameters::get_ContentType() const
```


## Ejemplos



Muestra cómo acceder a los parámetros de salida de la operación de guardado de un documento.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

// Después de guardar un documento, podemos acceder al Tipo de medio de Internet (tipo MIME) del documento de salida recién creado.
System::SharedPtr<Aspose::Words::Saving::SaveOutputParameters> parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.doc");

ASSERT_EQ(u"application/msword", parameters->get_ContentType());

// Esta propiedad cambia según el formato de guardado.
parameters = doc->Save(get_ArtifactsDir() + u"Document.SaveOutputParameters.pdf");

ASSERT_EQ(u"application/pdf", parameters->get_ContentType());
```

## Ver también

* Class [SaveOutputParameters](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
