---
title: "Método Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties. Obtiene BuiltInDocumentProperties del documento en C++."
type: docs
weight: 3000
url: /es/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Obtiene [BuiltInDocumentProperties](./) del documento.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Ejemplos



Muestra cómo cargar el contenido de un documento Microsoft Word en texto plano y luego acceder a las propiedades integradas del documento original.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_BuiltInDocumentProperties()->set_Author(u"John Doe");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.BuiltInProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASSERT_EQ(u"John Doe", plaintext->get_BuiltInDocumentProperties()->get_Author());
```

## Ver también

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
