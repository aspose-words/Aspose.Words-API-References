---
title: Aspose::Words::Saving::PdfDigitalSignatureDetails::PdfDigitalSignatureDetails constructor
linktitle: PdfDigitalSignatureDetails
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfDigitalSignatureDetails::PdfDigitalSignatureDetails constructor. Initializes an instance of this class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.saving/pdfdigitalsignaturedetails/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails::PdfDigitalSignatureDetails() constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfDigitalSignatureDetails::PdfDigitalSignatureDetails()
```

## See Also

* Class [PdfDigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
## PdfDigitalSignatureDetails::PdfDigitalSignatureDetails(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfDigitalSignatureDetails::PdfDigitalSignatureDetails(const System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> &certificateHolder, const System::String &reason, const System::String &location, System::DateTime signatureDate)
```


| Parameter | Type | Description |
| --- | --- | --- |
| certificateHolder | const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\& | A certificate holder which contains the certificate itself. |
| reason | const System::String\& | The reason for signing. |
| location | const System::String\& | The location of signing. |
| signatureDate | System::DateTime | The date and time of signing. |

## Examples



Shows how to sign a generated PDF document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Contents of signed PDF.");

SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Configure the "DigitalSignatureDetails" object of the "SaveOptions" object to
// digitally sign the document as we render it with the "Save" method.
System::DateTime signingTime = System::DateTime::get_Now();
options->set_DigitalSignatureDetails(MakeObject<PdfDigitalSignatureDetails>(certificateHolder, u"Test Signing", u"My Office", signingTime));
options->get_DigitalSignatureDetails()->set_HashAlgorithm(PdfDigitalSignatureHashAlgorithm::Sha256);

ASSERT_EQ(u"Test Signing", options->get_DigitalSignatureDetails()->get_Reason());
ASSERT_EQ(u"My Office", options->get_DigitalSignatureDetails()->get_Location());
ASSERT_EQ(signingTime.ToUniversalTime(), options->get_DigitalSignatureDetails()->get_SignatureDate().ToUniversalTime());

doc->Save(ArtifactsDir + u"PdfSaveOptions.PdfDigitalSignature.pdf", options);
```

## See Also

* Class [CertificateHolder](../../../aspose.words.digitalsignatures/certificateholder/)
* Class [PdfDigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
