---
title: get_DigitalSignatures
second_title: Aspose.Words for C++ API Reference
description: Gets the collection of digital signatures for this document and their validation results.
type: docs
weight: 248
url: /cpp/aspose.words/document/get_digitalsignatures/
---
## Document::get_DigitalSignatures method


Gets the collection of digital signatures for this document and their validation results.

```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureCollection> Aspose::Words::Document::get_DigitalSignatures() const
```

## Remarks


This collection contains digital signatures that were loaded from the original document. These digital signatures will not be saved when you save this [Document](../) object into a file or stream because saving or converting will produce a document that is different from the original and the original digital signatures will no longer be valid.

This collection is never null. If the document is not signed, it will contain zero elements.

## Examples



Shows how to validate and display information about each signature in a document. 
```cpp
auto doc = MakeObject<Document>(MyDir + u"Digitally signed.docx");

for (const auto& signature : doc->get_DigitalSignatures())
{
    std::cout << (signature->get_IsValid() ? String(u"Valid") : String(u"Invalid")) << " signature: " << std::endl;
    std::cout << "\tReason:\t" << signature->get_Comments() << std::endl;
    std::cout << String::Format(u"\tType:\t{0}", signature->get_SignatureType()) << std::endl;
    std::cout << "\tSign time:\t" << signature->get_SignTime() << std::endl;
    std::cout << "\tSubject name:\t" << signature->get_CertificateHolder()->get_Certificate()->get_SubjectName() << std::endl;
    std::cout << "\tIssuer name:\t" << signature->get_CertificateHolder()->get_Certificate()->get_IssuerName()->get_Name() << std::endl;
    std::cout << std::endl;
}
```


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

* Class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
