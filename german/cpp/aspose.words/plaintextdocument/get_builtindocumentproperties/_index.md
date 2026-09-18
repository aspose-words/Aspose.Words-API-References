---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties-Methode"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties-Methode. Ruft die BuiltInDocumentProperties des Dokuments in C++ ab."
type: docs
weight: 3000
url: /de/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Ruft die [BuiltInDocumentProperties](./) des Dokuments ab.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Beispiele



Zeigt, wie man den Inhalt eines Microsoft Word-Dokuments im Nur-Text-Format lädt und anschließend auf die integrierten Eigenschaften des Originaldokuments zugreift.
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

## Siehe auch

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
