---
title: PlainTextDocument
second_title: Aspose.Words for C++ API Reference
description: Allows to extract plain-text representation of the document's content.
type: docs
weight: 638
url: /cpp/aspose.words/plaintextdocument/
---
## PlainTextDocument class


Allows to extract plain-text representation of the document's content.

```cpp
class PlainTextDocument : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BuiltInDocumentProperties](./get_builtindocumentproperties/)() const | Gets [BuiltInDocumentProperties](./get_builtindocumentproperties/) of the document. |
| [get_CustomDocumentProperties](./get_customdocumentproperties/)() const | Gets [CustomDocumentProperties](./get_customdocumentproperties/) of the document. |
| [get_Text](./get_text/)() const | Gets textual content of the document concatenated as a string. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&) | Creates a plain text document from a file. Automatically detects the file format. |
| [PlainTextDocument](./plaintextdocument/)(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Creates a plain text document from a file. Allows to specify additional options such as an encryption password. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&) | Creates a plain text document from a stream. Automatically detects the file format. |
| [PlainTextDocument](./plaintextdocument/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) | Creates a plain text document from a stream. Allows to specify additional options such as an encryption password. |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&) |  |
| [PlainTextDocument](./plaintextdocument/)(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) |  |

## Examples



Shows how to load the contents of a Microsoft Word document in plaintext. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(ArtifactsDir + u"PlainTextDocument.Load.docx");

auto plaintext = MakeObject<PlainTextDocument>(ArtifactsDir + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## See Also

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
