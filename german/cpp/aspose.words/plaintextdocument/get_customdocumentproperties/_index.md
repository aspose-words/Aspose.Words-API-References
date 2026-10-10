---
title: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties-Methode"
linktitle: "get_CustomDocumentProperties"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::PlainTextDocument::get_CustomDocumentProperties-Methode. Ruft die CustomDocumentProperties des Dokuments in C++ ab."
type: docs
weight: 4000
url: /de/cpp/aspose.words/plaintextdocument/get_customdocumentproperties/
---
## PlainTextDocument::get_CustomDocumentProperties method


Ruft die [CustomDocumentProperties](./) des Dokuments ab.

```cpp
System::SharedPtr<Aspose::Words::Properties::CustomDocumentProperties> Aspose::Words::PlainTextDocument::get_CustomDocumentProperties() const
```


## Beispiele



Zeigt, wie man den Inhalt eines Microsoft Word-Dokuments im Nur-Text-Format lädt und anschließend auf die benutzerdefinierten Eigenschaften des Originaldokuments zugreift.
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

## Siehe auch

* Class [CustomDocumentProperties](../../../aspose.words.properties/customdocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
