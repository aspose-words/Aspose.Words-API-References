---
title: Aspose::Words::PlainTextDocument::PlainTextDocument constructor
linktitle: PlainTextDocument
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PlainTextDocument::PlainTextDocument constructor. Creates a plain text document from a stream. Automatically detects the file format in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/plaintextdocument/plaintextdocument/
---
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\> \&) constructor


Creates a plain text document from a stream. Automatically detects the file format.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> & stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\> \& | The stream where to extract the text from. |
## Remarks


 The document must be stored at the beginning of the stream. The stream must support random positioning. 
## Examples


Shows how to load the contents of a Microsoft Word document in plaintext using stream.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```
## Exceptions

* [UnsupportedFileFormatException](../../unsupportedfileformatexception/) - The document format is not recognized or not supported.
* [FileCorruptedException](../../filecorruptedexception/) - The document appears to be corrupted and cannot be loaded.
* **Exception** - There is a problem with the document and it should be reported to Aspose.Words developers.
* **IOException** - There is an input/output exception.
* [IncorrectPasswordException](../../incorrectpasswordexception/) - The document is encrypted and requires a password to open, but you supplied an incorrect password.
* **ArgumentNullException** - The stream cannot be null.
* **NotSupportedException** - The stream does not support reading or seeking.
* **ObjectDisposedException** - The stream is a disposed object.

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::SharedPtr\<System::IO::Stream\> \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) constructor


Creates a plain text document from a stream. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::SharedPtr<System::IO::Stream> & stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> & loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\> \& | The stream where to extract the text from. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \& | Additional options to use when loading a document. Can be **null**. |
## Remarks


 The document must be stored at the beginning of the stream. The stream must support random positioning. 
## Examples


Shows how to load the contents of an encrypted Microsoft Word document in plaintext using stream.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream, loadOptions);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```
## Exceptions

* [UnsupportedFileFormatException](../../unsupportedfileformatexception/) - The document format is not recognized or not supported.
* [FileCorruptedException](../../filecorruptedexception/) - The document appears to be corrupted and cannot be loaded.
* **Exception** - There is a problem with the document and it should be reported to Aspose.Words developers.
* **IOException** - There is an input/output exception.
* [IncorrectPasswordException](../../incorrectpasswordexception/) - The document is encrypted and requires a password to open, but you supplied an incorrect password.
* **ArgumentNullException** - The stream cannot be null.
* **NotSupportedException** - The stream does not support reading or seeking.
* **ObjectDisposedException** - The stream is a disposed object.

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String \&) constructor


Creates a plain text document from a file. Automatically detects the file format.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String & fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String \& | Name of the file to extract the text from. |
## Examples


Shows how to load the contents of a Microsoft Word document in plaintext.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.Load.docx");

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```
## Exceptions

* [UnsupportedFileFormatException](../../unsupportedfileformatexception/) - The document format is not recognized or not supported.
* [FileCorruptedException](../../filecorruptedexception/) - The document appears to be corrupted and cannot be loaded.
* **Exception** - There is a problem with the document and it should be reported to Aspose.Words developers.
* **IOException** - There is an input/output exception.
* [IncorrectPasswordException](../../incorrectpasswordexception/) - The document is encrypted and requires a password to open, but you supplied an incorrect password.
* **ArgumentException** - The name of the file cannot be null or empty string.

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(const System::String \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) constructor


Creates a plain text document from a file. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(const System::String & fileName, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> & loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String \& | Name of the file to extract the text from. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \& | Additional options to use when loading a document. Can be **null**. |
## Remarks

## Examples


Shows how to load the contents of an encrypted Microsoft Word document in plaintext.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(get_ArtifactsDir() + u"PlainTextDocument.LoadEncrypted.docx", loadOptions);

ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
```
## Exceptions

* [UnsupportedFileFormatException](../../unsupportedfileformatexception/) - The document format is not recognized or not supported.
* [FileCorruptedException](../../filecorruptedexception/) - The document appears to be corrupted and cannot be loaded.
* **Exception** - There is a problem with the document and it should be reported to Aspose.Words developers.
* **IOException** - There is an input/output exception.
* [IncorrectPasswordException](../../incorrectpasswordexception/) - The document is encrypted and requires a password to open, but you supplied an incorrect password.
* **ArgumentException** - The name of the file cannot be null or empty string.

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream \&) constructor


Creates a plain text document from a stream. Automatically detects the file format.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream & stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | std::istream \& | The stream where to extract the text from. |
## Remarks


 The document must be stored at the beginning of the stream. The stream must support random positioning. 
## Examples


Shows how to load the contents of a Microsoft Word document in plaintext using stream.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStream.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```
## Exceptions

* [UnsupportedFileFormatException](../../unsupportedfileformatexception/) - The document format is not recognized or not supported.
* [FileCorruptedException](../../filecorruptedexception/) - The document appears to be corrupted and cannot be loaded.
* **Exception** - There is a problem with the document and it should be reported to Aspose.Words developers.
* **IOException** - There is an input/output exception.
* [IncorrectPasswordException](../../incorrectpasswordexception/) - The document is encrypted and requires a password to open, but you supplied an incorrect password.
* **ArgumentNullException** - The stream cannot be null.
* **NotSupportedException** - The stream does not support reading or seeking.
* **ObjectDisposedException** - The stream is a disposed object.

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## PlainTextDocument::PlainTextDocument(std::istream \&, const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \&) constructor


Creates a plain text document from a stream. Allows to specify additional options such as an encryption password.

```cpp
Aspose::Words::PlainTextDocument::PlainTextDocument(std::istream & stream, const System::SharedPtr<Aspose::Words::Loading::LoadOptions> & loadOptions)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | std::istream \& | The stream where to extract the text from. |
| loadOptions | const System::SharedPtr\<Aspose::Words::Loading::LoadOptions\> \& | Additional options to use when loading a document. Can be **null**. |
## Remarks


 The document must be stored at the beginning of the stream. The stream must support random positioning. 
## Examples


Shows how to load the contents of an encrypted Microsoft Word document in plaintext using stream.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::OoxmlSaveOptions>();
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", saveOptions);

auto loadOptions = System::MakeObject<Aspose::Words::Loading::LoadOptions>();
loadOptions->set_Password(u"MyPassword");

{
    auto stream = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"PlainTextDocument.LoadFromStreamWithOptions.docx", System::IO::FileMode::Open);
    auto plaintext = System::MakeObject<Aspose::Words::PlainTextDocument>(stream, loadOptions);

    ASSERT_EQ(u"Hello world!", plaintext->get_Text().Trim());
}
```
## Exceptions

* [UnsupportedFileFormatException](../../unsupportedfileformatexception/) - The document format is not recognized or not supported.
* [FileCorruptedException](../../filecorruptedexception/) - The document appears to be corrupted and cannot be loaded.
* **Exception** - There is a problem with the document and it should be reported to Aspose.Words developers.
* **IOException** - There is an input/output exception.
* [IncorrectPasswordException](../../incorrectpasswordexception/) - The document is encrypted and requires a password to open, but you supplied an incorrect password.
* **ArgumentNullException** - The stream cannot be null.
* **NotSupportedException** - The stream does not support reading or seeking.
* **ObjectDisposedException** - The stream is a disposed object.

## See Also

* Class [PlainTextDocument](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
