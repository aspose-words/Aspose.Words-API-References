---
title: Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures method
linktitle: RemoveAllSignatures
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures method. Removes all digital signatures from document in source stream and writes unsigned document to destination stream. Output will be written to the start of stream and stream size will be updated with content length.The following formats are compatible for digital signature removal: Doc, Dot, Docx, Dotx, Docm, Odt, Ott in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.digitalsignatures/digitalsignatureutil/removeallsignatures/
---
## DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr\<System::IO::Stream\>\&, const System::SharedPtr\<System::IO::Stream\>\&) method


Removes all digital signatures from document in source stream and writes unsigned document to destination stream. **Output will be written to the start of stream and stream size will be updated with content length.**The following formats are compatible for digital signature removal: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::SharedPtr<System::IO::Stream> &srcStream, const System::SharedPtr<System::IO::Stream> &dstStream)
```


## Examples



Shows how to remove digital signatures from a digitally signed document. 
```cpp
// There are two ways of using the DigitalSignatureUtil class to remove digital signatures
// from a signed document by saving an unsigned copy of it somewhere else in the local file system.
// 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
DigitalSignatureUtil::RemoveAllSignatures(MyDir + u"Digitally signed.docx", ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
{
    SharedPtr<System::IO::Stream> streamIn = MakeObject<System::IO::FileStream>(MyDir + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        SharedPtr<System::IO::Stream> streamOut =
            MakeObject<System::IO::FileStream>(ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verify that both our output documents have no digital signatures.
ASSERT_EQ(0, DigitalSignatureUtil::LoadSignatures(ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, DigitalSignatureUtil::LoadSignatures(ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(const System::String\&, const System::String\&) method


Removes all digital signatures from source file and writes unsigned file to destination file. The following formats are compatible for digital signature removal: [Doc](../../../aspose.words/loadformat/), [Dot](../../../aspose.words/loadformat/), [Docx](../../../aspose.words/loadformat/), [Dotx](../../../aspose.words/loadformat/), [Docm](../../../aspose.words/loadformat/), [Odt](../../../aspose.words/loadformat/), [Ott](../../../aspose.words/loadformat/).

```cpp
static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(const System::String &srcFileName, const System::String &dstFileName)
```


## Examples



Shows how to remove digital signatures from a digitally signed document. 
```cpp
// There are two ways of using the DigitalSignatureUtil class to remove digital signatures
// from a signed document by saving an unsigned copy of it somewhere else in the local file system.
// 1 - Determine the locations of both the signed document and the unsigned copy by filename strings:
DigitalSignatureUtil::RemoveAllSignatures(MyDir + u"Digitally signed.docx", ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx");

// 2 - Determine the locations of both the signed document and the unsigned copy by file streams:
{
    SharedPtr<System::IO::Stream> streamIn = MakeObject<System::IO::FileStream>(MyDir + u"Digitally signed.docx", System::IO::FileMode::Open);
    {
        SharedPtr<System::IO::Stream> streamOut =
            MakeObject<System::IO::FileStream>(ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::RemoveAllSignatures(streamIn, streamOut);
    }
}

// Verify that both our output documents have no digital signatures.
ASSERT_EQ(0, DigitalSignatureUtil::LoadSignatures(ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromString.docx")->get_Count());
ASSERT_EQ(0, DigitalSignatureUtil::LoadSignatures(ArtifactsDir + u"DigitalSignatureUtil.LoadAndRemove.FromStream.docx")->get_Count());
```

## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream\<CharType, Traits\>\&, std::basic_ostream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static void Aspose::Words::DigitalSignatures::DigitalSignatureUtil::RemoveAllSignatures(std::basic_istream<CharType, Traits> &srcStream, std::basic_ostream<CharType, Traits> &dstStream)
```

## See Also

* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
