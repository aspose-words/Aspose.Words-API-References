---
title: "Método Aspose::Words::Document::get_RemovePersonalInformation"
linktitle: "get_RemovePersonalInformation"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::Document::get_RemovePersonalInformation. Obtiene o establece una bandera que indica que Microsoft Word eliminará toda la información del usuario de los comentarios, revisiones y propiedades del documento al guardar el documento en C++."
type: docs
weight: 45000
url: /es/cpp/aspose.words/document/get_removepersonalinformation/
---
## Document::get_RemovePersonalInformation method


Obtiene o establece una bandera que indica que Microsoft Word eliminará toda la información del usuario de los comentarios, revisiones y propiedades del documento al guardar el documento.

```cpp
bool Aspose::Words::Document::get_RemovePersonalInformation()
```


## Ejemplos



Muestra cómo habilitar la eliminación de información personal durante un guardado manual.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserte contenido con información personal.
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");
doc->get_BuiltInDocumentProperties()->set_Company(u"Placeholder Inc.");

doc->StartTrackRevisions(doc->get_BuiltInDocumentProperties()->get_Author(), System::DateTime::get_Now());
builder->Write(u"Hello world!");
doc->StopTrackRevisions();

// Esta bandera equivale a Archivo -> Opciones -> Centro de confianza -> Configuración del Centro de confianza... ->
// Opciones de privacidad -> "Eliminar información personal de las propiedades del archivo al guardar" en Microsoft Word.
doc->set_RemovePersonalInformation(saveWithoutPersonalInfo);

// Esta opción no tendrá efecto durante una operación de guardado realizada con Aspose.Words.
// Los datos personales se eliminarán de nuestro documento con la bandera activada cuando lo guardemos manualmente usando Microsoft Word.
doc->Save(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");
doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Document.RemovePersonalInformation.docx");

ASPOSE_ASSERT_EQ(saveWithoutPersonalInfo, doc->get_RemovePersonalInformation());
ASSERT_EQ(u"John Doe", doc->get_BuiltInDocumentProperties()->get_Author());
ASSERT_EQ(u"Placeholder Inc.", doc->get_BuiltInDocumentProperties()->get_Company());
ASSERT_EQ(u"John Doe", doc->get_Revisions()->idx_get(0)->get_Author());
```

## Ver también

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
