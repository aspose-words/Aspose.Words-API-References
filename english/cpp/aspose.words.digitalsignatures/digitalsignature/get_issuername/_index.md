---
title: Aspose::Words::DigitalSignatures::DigitalSignature::get_IssuerName method
linktitle: get_IssuerName
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignature::get_IssuerName method. Returns the subject distinguished name of the certificate isuuer in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.digitalsignatures/digitalsignature/get_issuername/
---
## DigitalSignature::get_IssuerName method


Returns the subject distinguished name of the certificate isuuer.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignature::get_IssuerName()
```


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

* Class [DigitalSignature](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
