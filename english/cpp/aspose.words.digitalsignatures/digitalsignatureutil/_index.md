---
title: Aspose::Words::DigitalSignatures::DigitalSignatureUtil class
linktitle: DigitalSignatureUtil
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureUtil class. Provides methods for signing document. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.digitalsignatures/digitalsignatureutil/
---
## DigitalSignatureUtil class


Provides methods for signing document. To learn more, visit the [Work with Digital Signatures](https://docs.aspose.com/words/cpp/working-with-digital-signatures/) documentation article.

```cpp
class DigitalSignatureUtil
```

## Methods

| Method | Description |
| --- | --- |
| [DigitalSignatureUtil](./digitalsignatureutil/)() |  |
| static [LoadSignatures](./loadsignatures/)(const System::String\&) | Loads digital signatures from document. |
| static [LoadSignatures](./loadsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&) | Loads digital signatures from document using stream. |
| static [LoadSignatures](./loadsignatures/)(std::basic_istream\<CharType, Traits\>\&) |  |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::String\&, const System::String\&) | Removes all digital signatures from source file and writes unsigned file to destination file. The following formats are compatible for digital signature removal: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) | Removes all digital signatures from document in source stream and writes unsigned document to destination stream. **Output will be written to the start of stream and stream size will be updated with content length.**The following formats are compatible for digital signature removal: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [RemoveAllSignatures](./removeallsignatures/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) |  |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Signs source document using given [CertificateHolder](../certificateholder/) and [SignOptions](../signoptions/) with digital signature and writes signed document to destination stream. Supported formats are: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**Output will be written to the start of stream and stream size will be updated with content length.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>\&) | Signs source document using given [CertificateHolder](../certificateholder/) and [SignOptions](../signoptions/) with digital signature and writes signed document to destination file. Supported formats are: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Signs source document using given [CertificateHolder](../certificateholder/) with digital signature and writes signed document to destination stream. Supported formats are: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).**Output will be written to the start of stream and stream size will be updated with content length.** |
| static [Sign](./sign/)(const System::String\&, const System::String\&, const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Signs source document using given [CertificateHolder](../certificateholder/) with digital signature and writes signed document to destination file. Supported formats are: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/). |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>, System::SharedPtr\<Aspose::Words::DigitalSignatures::SignOptions\>) |  |
| static [Sign](./sign/)(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&, System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>) |  |
## Remarks


Since digital signature works with file content rather than [Document](../../aspose.words/document/) Object Model these methods are put into a separate class.

Supported formats are: [Doc](../../aspose.words/loadformat/), [Dot](../../aspose.words/loadformat/), [Docx](../../aspose.words/loadformat/), [Dotx](../../aspose.words/loadformat/), [Docm](../../aspose.words/loadformat/), [Dotm](../../aspose.words/loadformat/), [Odt](../../aspose.words/loadformat/), [Ott](../../aspose.words/loadformat/).

## Examples



Shows how to load signatures from a digitally signed document. 
```cpp
// There are two ways of loading a signed document's collection of digital signatures using the DigitalSignatureUtil class.
// 1 -  Load from a document from a local file system filename:
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_MyDir() + u"Digitally signed.docx");

// If this collection is nonempty, then we can verify that the document is digitally signed.
ASSERT_EQ(1, digitalSignatures->get_Count());

// 2 -  Load from a document from a FileStream:
{
    System::SharedPtr<System::IO::Stream> stream = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    digitalSignatures = Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(stream);
    ASSERT_EQ(1, digitalSignatures->get_Count());
}
```


Shows how to remove digital signatures from a digitally signed document. 
```cpp
// There are two ways of using the DigitalSignatureUtil class to remove digital signatures
// from a signed document by saving an unsigned copy of it somewhere else in the local file system.
// 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
{
    System::SharedPtr<System::IO::Stream> streamIn = System::MakeObject<System::IO::FileStream>(get_MyDir() + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        System::SharedPtr<System::IO::Stream> streamOut = System::MakeObject<System::IO::FileStream>(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verify that both our output documents have no digital signatures.
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
