---
title: PdfDigitalSignatureDetails
second_title: Aspose.Words for C++ API Reference
description: Contains details for signing a PDF document with a digital signature.
type: docs
weight: 274
url: /cpp/aspose.words.saving/pdfdigitalsignaturedetails/
---
## PdfDigitalSignatureDetails class


Contains details for signing a PDF document with a digital signature.

```cpp
class PdfDigitalSignatureDetails : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_CertificateHolder](./get_certificateholder/)() const | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [get_HashAlgorithm](./get_hashalgorithm/)() const | Gets or sets the hash algorithm. |
| [get_Location](./get_location/)() const | Gets or sets the location of the signing. |
| [get_Reason](./get_reason/)() const | Gets or sets the reason for the signing. |
| [get_SignatureDate](./get_signaturedate/)() const | Gets or sets the date of the signing. |
| [get_TimestampSettings](./get_timestampsettings/)() const | Gets or sets the digital signature timestamp settings. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)() | Initializes an instance of this class. |
| [PdfDigitalSignatureDetails](./pdfdigitalsignaturedetails/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&, const System::String\&, const System::String\&, System::DateTime) | Initializes an instance of this class. |
| [set_CertificateHolder](./set_certificateholder/)(const System::SharedPtr\<Aspose::Words::DigitalSignatures::CertificateHolder\>\&) | Returns the certificate holder object that contains the certificate was used to sign the document. |
| [set_HashAlgorithm](./set_hashalgorithm/)(Aspose::Words::Saving::PdfDigitalSignatureHashAlgorithm) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_HashAlgorithm](./get_hashalgorithm/). |
| [set_Location](./set_location/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_Location](./get_location/). |
| [set_Reason](./set_reason/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_Reason](./get_reason/). |
| [set_SignatureDate](./set_signaturedate/)(System::DateTime) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_SignatureDate](./get_signaturedate/). |
| [set_TimestampSettings](./set_timestampsettings/)(const System::SharedPtr\<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings\>\&) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings](./get_timestampsettings/). |
## Remarks


At the moment digitally signing PDF documents is only available on .NET 2.0 or higher.

To digitally sign a PDF document when it is created by Aspose.Words, set the [DigitalSignatureDetails](../pdfsaveoptions/get_digitalsignaturedetails/) property to a valid [PdfDigitalSignatureDetails](./) object and then save the document in the PDF format passing the [PdfSaveOptions](../pdfsaveoptions/) as a parameter into the [Save()](../) method.

Aspose.Words creates a PKCS#7 signature over the whole PDF document and uses the "Adobe.PPKMS" filter and "adbe.pkcs7.sha1" subfilter when creating a digital signature.

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
