---
title: Aspose::Words::DigitalSignatures::DigitalSignatureType enum
linktitle: DigitalSignatureType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureType enum. Specifies the type of a digital signature in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.digitalsignatures/digitalsignaturetype/
---
## DigitalSignatureType enum


Specifies the type of a digital signature.

```cpp
enum class DigitalSignatureType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Unknown | 0 | Indicates an error, unknown digital signature type. |
| CryptoApi | 1 | The Crypto API signature method used in Microsoft Word 97-2003 .DOC binary documents. |
| XmlDsig | 2 | The XmlDsig signature method used in OOXML and OpenDocument documents. |


## Examples



Shows how to sign documents with X.509 certificates. 
```cpp
// Verify that a document is not signed.
ASSERT_FALSE(FileFormatUtil::DetectFileFormat(MyDir + u"Document.docx")->get_HasDigitalSignature());

// Create a CertificateHolder object from a PKCS12 file, which we will use to sign the document.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw", nullptr);

// There are two ways of saving a signed copy of a document to the local file system:
// 1 - Designate a document by a local system filename and save a signed copy at a location specified by another filename.
auto signOptions = MakeObject<SignOptions>();
signOptions->set_SignTime(System::DateTime::get_Now());

DigitalSignatureUtil::Sign(MyDir + u"Document.docx", ArtifactsDir + u"Document.DigitalSignature.docx", certificateHolder, signOptions);

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(ArtifactsDir + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// 2 - Take a document from a stream and save a signed copy to another stream.
{
    auto inDoc = MakeObject<System::IO::FileStream>(MyDir + u"Document.docx", System::IO::FileMode::Open);
    {
        auto outDoc = MakeObject<System::IO::FileStream>(ArtifactsDir + u"Document.DigitalSignature.docx", System::IO::FileMode::Create);
        DigitalSignatureUtil::Sign(inDoc, outDoc, certificateHolder);
    }
}

ASSERT_TRUE(FileFormatUtil::DetectFileFormat(ArtifactsDir + u"Document.DigitalSignature.docx")->get_HasDigitalSignature());

// Please verify that all of the document's digital signatures are valid and check their details.
auto signedDoc = MakeObject<Document>(ArtifactsDir + u"Document.DigitalSignature.docx");
SharedPtr<DigitalSignatureCollection> digitalSignatureCollection = signedDoc->get_DigitalSignatures();

ASSERT_TRUE(digitalSignatureCollection->get_IsValid());
ASSERT_EQ(1, digitalSignatureCollection->get_Count());
ASSERT_EQ(DigitalSignatureType::XmlDsig, digitalSignatureCollection->idx_get(0)->get_SignatureType());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_IssuerName());
ASSERT_EQ(u"CN=Morzal.Me", signedDoc->get_DigitalSignatures()->idx_get(0)->get_SubjectName());
```

## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
