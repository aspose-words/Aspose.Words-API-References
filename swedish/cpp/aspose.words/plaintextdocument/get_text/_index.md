---
title: "Aspose::Words::PlainTextDocument::get_Text metod"
linktitle: "get_Text"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PlainTextDocument::get_Text metod. Hämtar dokumentets textinnehåll sammanslaget som en sträng i C++."
type: docs
weight: 5000
url: /sv/cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Hämtar textinnehållet i dokumentet sammanfogat som en sträng.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


## Exempel



Visar hur man laddar innehållet i ett Microsoft Word-dokument i rentext.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## Se även

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
