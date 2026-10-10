---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties metodo"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties metodo. Ottiene le BuiltInDocumentProperties del documento in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Ottiene [BuiltInDocumentProperties](./) del documento.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word in testo semplice e quindi accedere alle proprietà integrate del documento originale.
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

## Vedi anche

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
