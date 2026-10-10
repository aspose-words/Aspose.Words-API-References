---
title: "Aspose::Words::PlainTextDocument klass"
linktitle: "PlainTextDocument"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::PlainTextDocument klass. Tillåter att extrahera en rentextrepresentation av dokumentets innehåll. För att lära dig mer, besök dokumentationsartikeln i C++."
type: docs
weight: 50000
url: /sv/cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Tillåter att extrahera en rentextrepresentation av dokumentets innehåll. För att lära dig mer, besök dokumentationsartikeln [Working with Text Document](https://docs.aspose.com/words/cpp/working-with-text-document/).

```cpp
class PlainTextDocument : public System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Hämtar [BuiltInDocumentProperties](./get_builtindocumentproperties/) för dokumentet. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Hämtar [CustomDocumentProperties](./get_customdocumentproperties/) för dokumentet. |
| [get_Text](./get_text/)() const | Hämtar textinnehållet i dokumentet sammanfogat som en sträng. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Skapar ett rentextdokument från en fil. Upptäcker automatiskt filformatet. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Skapar ett rentextdokument från en fil. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Skapar ett rentextdokument från en ström. Upptäcker automatiskt filformatet. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Skapar ett rentextdokument från en ström. Tillåter att ange ytterligare alternativ såsom ett krypteringslösenord. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
