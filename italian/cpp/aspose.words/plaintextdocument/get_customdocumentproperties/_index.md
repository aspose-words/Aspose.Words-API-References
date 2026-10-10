---
title: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties metodo"
linktitle: "get_CustomDocumentProperties"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties metodo. Ottiene le CustomDocumentProperties del documento in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/plaintextdocument/get_customdocumentproperties/
---
## PlainTextDocument::get_CustomDocumentProperties method


Ottiene [CustomDocumentProperties](./) del documento.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::PlainTextDocument::get_CustomDocumentProperties() const
```


## Esempi



Mostra come caricare il contenuto di un documento Microsoft Word in testo semplice e quindi accedere alle proprietà personalizzate del documento originale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->get_CustomDocumentProperties()->Add(u"Location of writing", System::String(u"123 Main St, London, UK"));

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.CustomDocumentProperties.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
ASPOSE_ASSERT_EQ(u"123 Main St, London, UK", plaintext->get_CustomDocumentProperties()->idx_get(u"Location of writing")->get_Value());
```

## Vedi anche

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
