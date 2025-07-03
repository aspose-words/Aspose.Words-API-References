---
title: Aspose::Words::FileFormatUtil::DetectFileFormat method
linktitle: DetectFileFormat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::FileFormatUtil::DetectFileFormat method. Detects and returns the information about a format of a document stored in a stream in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/fileformatutil/detectfileformat/
---
## FileFormatUtil::DetectFileFormat(const System::SharedPtr\<System::IO::Stream\>\&) method


Detects and returns the information about a format of a document stored in a stream.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::SharedPtr<System::IO::Stream> &stream)
```


| Parameter | Type | Description |
| --- | --- | --- |
| stream | const System::SharedPtr\<System::IO::Stream\>\& | The stream. |

### ReturnValue

A [FileFormatInfo](../../fileformatinfo/) object that contains the detected information.
## Remarks


The stream must be positioned at the beginning of the document.

When this method returns, the position in the stream is restored to the original position.

Even if this method detects the document format, it does not guarantee that the specified document is valid. This method only detects the document format by reading data that is sufficient for detection. To fully verify that a document is valid you need to load the document into a [Document](../../document/) object.

This method throws [FileCorruptedException](../../filecorruptedexception/) when the format is recognized, but the detection cannot complete because of corruption.

## Examples



Shows how to use the [FileFormatUtil](../) methods to detect the format of a document. 
```cpp
// Load a document from a file that is missing a file extension, and then detect its file format.
{
    System::SharedPtr<System::IO::FileStream> docStream = System::IO::File::OpenRead(get_MyDir() + u"Word document with missing file extension");
    System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(docStream);
    Aspose::Words::LoadFormat loadFormat = info->get_LoadFormat();

    ASSERT_EQ(Aspose::Words::LoadFormat::Doc, loadFormat);

    // Below are two methods of converting a LoadFormat to its corresponding SaveFormat.
    // 1 -  Get the file extension string for the LoadFormat, then get the corresponding SaveFormat from that string:
    System::String fileExtension = Aspose::Words::FileFormatUtil::LoadFormatToExtension(loadFormat);
    Aspose::Words::SaveFormat saveFormat = Aspose::Words::FileFormatUtil::ExtensionToSaveFormat(fileExtension);

    // 2 -  Convert the LoadFormat directly to its SaveFormat:
    saveFormat = Aspose::Words::FileFormatUtil::LoadFormatToSaveFormat(loadFormat);

    // Load a document from the stream, and then save it to the automatically detected file extension.
    auto doc = System::MakeObject<Aspose::Words::Document>(docStream);

    ASSERT_EQ(u".doc", Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));

    doc->Save(get_ArtifactsDir() + u"File.SaveToDetectedFileFormat" + Aspose::Words::FileFormatUtil::SaveFormatToExtension(saveFormat));
}
```

## See Also

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(const System::String\&) method


Detects and returns the information about a format of a document stored in a disk file.

```cpp
static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(const System::String &fileName)
```


| Parameter | Type | Description |
| --- | --- | --- |
| fileName | const System::String\& | The file name. |

### ReturnValue

A [FileFormatInfo](../../fileformatinfo/) object that contains the detected information.
## Remarks


Even if this method detects the document format, it does not guarantee that the specified document is valid. This method only detects the document format by reading data that is sufficient for detection. To fully verify that a document is valid you need to load the document into a [Document](../../document/) object.

This method throws [FileCorruptedException](../../filecorruptedexception/) when the format is recognized, but the detection cannot complete because of corruption.

## Examples



Shows how to use the [FileFormatUtil](../) class to detect the document format and encryption. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Configure a SaveOptions object to encrypt the document
// with a password when we save it, and then save the document.
auto saveOptions = System::MakeObject<Aspose::Words::Saving::OdtSaveOptions>(Aspose::Words::SaveFormat::Odt);
saveOptions->set_Password(u"MyPassword");

doc->Save(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt", saveOptions);

// Verify the file type of our document, and its encryption status.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDocumentEncryption.odt");

ASSERT_EQ(u".odt", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_TRUE(info->get_IsEncrypted());
```


Shows how to use the [FileFormatUtil](../) class to detect the document format and presence of digital signatures. 
```cpp
// Use a FileFormatInfo instance to verify that a document is not digitally signed.
System::SharedPtr<Aspose::Words::FileFormatInfo> info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_MyDir() + u"Document.docx");

ASSERT_EQ(u".docx", Aspose::Words::FileFormatUtil::LoadFormatToExtension(info->get_LoadFormat()));
ASSERT_FALSE(info->get_HasDigitalSignature());

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw", nullptr);
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(get_MyDir() + u"Document.docx", get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx", certificateHolder, signOptions);

// Use a new FileFormatInstance to confirm that it is signed.
info = Aspose::Words::FileFormatUtil::DetectFileFormat(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx");

ASSERT_TRUE(info->get_HasDigitalSignature());

// We can load and access the signatures of a signed document in a collection like this.
ASSERT_EQ(1, Aspose::Words::DigitalSignatures::DigitalSignatureUtil::LoadSignatures(get_ArtifactsDir() + u"File.DetectDigitalSignatures.docx")->get_Count());
```

## See Also

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## FileFormatUtil::DetectFileFormat(std::basic_istream\<CharType, Traits\>\&) method




```cpp
template<typename CharType,typename Traits> static System::SharedPtr<Aspose::Words::FileFormatInfo> Aspose::Words::FileFormatUtil::DetectFileFormat(std::basic_istream<CharType, Traits> &stream)
```

## See Also

* Class [FileFormatInfo](../../fileformatinfo/)
* Class [FileFormatUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
