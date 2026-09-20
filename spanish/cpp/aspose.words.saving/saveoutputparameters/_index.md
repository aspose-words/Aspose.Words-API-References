---
title: "Clase Aspose::Words::Saving::SaveOutputParameters"
linktitle: "SaveOutputParameters"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Clase Aspose::Words::Saving::SaveOutputParameters. Este objeto se devuelve al llamador después de que se guarda un documento y contiene información adicional que se ha generado o calculado durante la operación de guardado. El llamador puede usar o ignorar este objeto. Para obtener más información, visite el artículo de documentación en C++."
type: docs
weight: 30000
url: /es/cpp/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class


Este objeto se devuelve al llamador después de que se guarda un documento y contiene información adicional que se ha generado o calculado durante la operación de guardado. El llamador puede usar o ignorar este objeto. Para obtener más información, visite el artículo de documentación [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class SaveOutputParameters : public System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| [get_ContentType](./get_contenttype/)() const | Devuelve la cadena Content-Type (Tipo de medio de Internet) que identifica el tipo del documento guardado. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
