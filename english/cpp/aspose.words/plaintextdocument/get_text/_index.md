---
title: get_Text
second_title: Aspose.Words for C++ API Reference
description: Gets textual content of the document concatenated as a string.
type: docs
weight: 53
url: /cpp/aspose.words/plaintextdocument/get_text/
---
## PlainTextDocument::get_Text method


Gets textual content of the document concatenated as a string.

```cpp
System::String Aspose::Words::PlainTextDocument::get_Text() const
```


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

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
