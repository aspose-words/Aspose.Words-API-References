---
title: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties metod"
linktitle: "get_BuiltInDocumentProperties"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties metod. Hämtar BuiltInDocumentProperties för dokumentet i C++."
type: docs
weight: 3000
url: /sv/cpp/aspose.words/plaintextdocument/get_builtindocumentproperties/
---
## PlainTextDocument::get_BuiltInDocumentProperties method


Hämtar [BuiltInDocumentProperties](./) för dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Properties::BuiltInDocumentProperties> Aspose::Words::PlainTextDocument::get_BuiltInDocumentProperties() const
```


## Exempel



Visar hur man laddar innehållet i ett Microsoft Word-dokument i klartext och sedan får åtkomst till dokumentets inbyggda egenskaper.
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

## Se även

* Class [BuiltInDocumentProperties](../../../aspose.words.properties/builtindocumentproperties/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
