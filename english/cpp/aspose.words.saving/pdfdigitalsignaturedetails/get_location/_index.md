---
title: Aspose::Words::Saving::PdfDigitalSignatureDetails::get_Location method
linktitle: get_Location
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::PdfDigitalSignatureDetails::get_Location method. Gets or sets the location of the signing in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words.saving/pdfdigitalsignaturedetails/get_location/
---
## PdfDigitalSignatureDetails::get_Location method


Gets or sets the location of the signing.

```cpp
System::String Aspose::Words::Saving::PdfDigitalSignatureDetails::get_Location() const
```


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

* Class [PdfDigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
