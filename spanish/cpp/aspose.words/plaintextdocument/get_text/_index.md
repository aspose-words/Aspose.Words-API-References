---
title: "Método Aspose::Words::PlainTextDocument::get_Text"
linktitle: "get_Text"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::PlainTextDocument::get_Text. Obtiene el contenido textual del documento concatenado como una cadena en C++."
type: docs
weight: 5000
url: /es/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Obtiene el contenido textual del documento concatenado como una cadena.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## Ejemplos



Muestra cómo cargar el contenido de un documento Microsoft Word en texto sin formato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Ver también

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
