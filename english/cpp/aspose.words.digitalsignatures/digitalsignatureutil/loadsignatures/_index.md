---
title: Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method
linktitle: LoadSignatures
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures method. Loads digital signatures from document using stream in C++.'
type: docs
weight: 1000
url: /cpp/aspose.words.digitalsignatures/digitalsignatureutil/loadsignatures/
---
## DigitalSignatureUtil::LoadSignatures(const System::SharedPtr\<System::IO::Stream\>\&) method


Loads digital signatures from document using stream.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | Stream with the document. |

### ReturnValue

Collection of digital signatures. Returns empty collection if file is not signed.

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

## See Also

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(const System::String\&) method


Loads digital signatures from document.

```cpp
static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | Path to the document. |

### ReturnValue

Collection of digital signatures. Returns empty collection if file is not signed.

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

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
## DigitalSignatureUtil::LoadSignatures(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(std::basic_istream<CharType, Traits> &stream)
```

## See Also

* Class [DigitalSignatureCollection](../../digitalsignaturecollection/)
* Class [DigitalSignatureUtil](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
