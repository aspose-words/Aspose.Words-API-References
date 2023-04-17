---
title: Aspose::Words::PlainTextDocument::PlainTextDocument constructor
linktitle: PlainTextDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PlainTextDocument::PlainTextDocument constructor. Creates a plain text document from a stream. Automatically detects the file format in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&) constructor


Creates a plain text document from a stream. Automatically detects the file format.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream where to extract the text from. |
## Remarks


The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples



Shows how to load the contents of a Microsoft Word document in plaintext using stream. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->Save(ArtifactsDir + u"PlainTextDocument.LoadFromStream.docx");

{
    auto stream = MakeObject<System::IO::FileStream>(ArtifactsDir + u"PlainTextDocument.LoadFromStream.docx", System::IO::FileMode::Open);
    auto plaintext = MakeObject<PlainTextDocument>(stream);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Creates a plain text document from a stream. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream where to extract the text from. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Additional options to use when loading a document. Can be **null**. |
## Remarks


The document must be stored at the beginning of the stream. The stream must support random positioning.

## Examples



Shows how to load the contents of an encrypted Microsoft Word document in plaintext using stream. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(ArtifactsDir + u"PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_Password(u"MyPassword");

{
    auto stream = MakeObject<System::IO::FileStream>(ArtifactsDir + u"PlainTextDocument.LoadFromStreamWithOptions.docx", System::IO::FileMode::Open);
    auto plaintext = MakeObject<PlainTextDocument>(stream, loadOptions);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&) constructor


Creates a plain text document from a file. Automatically detects the file format.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Name of the file to extract the text from. |

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
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor


Creates a plain text document from a file. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String &fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Name of the file to extract the text from. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\& | Additional options to use when loading a document. Can be **null**. |

## Examples



Shows how to load the contents of an encrypted Microsoft Word document in plaintext. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = MakeObject<OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(ArtifactsDir + u"PlainTextDocument.LoadEncrypted.docx", saveOptions);

auto loadOptions = MakeObject<LoadOptions>();
loadOptions->set_Password(u"MyPassword");

auto plaintext = MakeObject<PlainTextDocument>(ArtifactsDir + u"PlainTextDocument.LoadEncrypted.docx", loadOptions);

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream)
```

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream\&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\>\&) constructor




```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream &stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> &loadOptions)
```

## See Also

* Class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
