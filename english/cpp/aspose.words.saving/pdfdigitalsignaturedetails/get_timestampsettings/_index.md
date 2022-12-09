---
title: get_TimestampSettings
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the digital signature timestamp settings.
type: docs
weight: 92
url: /cpp/aspose.words.saving/pdfdigitalsignaturedetails/get_timestampsettings/
---
## PdfDigitalSignatureDetails::get_TimestampSettings method


Gets or sets the digital signature timestamp settings.

```cpp
System::SharedPtr<Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings> Aspose::Words::Saving::PdfDigitalSignatureDetails::get_TimestampSettings() const
```

## Remarks


The default value is **null** and the digital signature will not be time-stamped. When this property is set to a valid [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/) object, then the digital signature in the PDF document will be time-stamped.

## Examples



Shows how to sign a saved PDF document digitally and timestamp it. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Signed PDF contents.");

// Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
// to modify how that method converts the document to .PDF.
auto options = MakeObject<PdfSaveOptions>();

// Create a digital signature and assign it to our SaveOptions object to sign the document when we save it to PDF.
SharedPtr<CertificateHolder> certificateHolder = CertificateHolder::Create(MyDir + u"morzal.pfx", u"aw");
options->set_DigitalSignatureDetails(
    MakeObject<PdfDigitalSignatureDetails>(certificateHolder, u"Test Signing", u"Aspose Office", System::DateTime::get_Now()));

// Create a timestamp authority-verified timestamp.
options->get_DigitalSignatureDetails()->set_TimestampSettings(
    MakeObject<PdfDigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword"));

// The default lifespan of the timestamp is 100 seconds.
ASPOSE_ASSERT_EQ(100.0, options->get_DigitalSignatureDetails()->get_TimestampSettings()->get_Timeout().get_TotalSeconds());

// We can set our timeout period via the constructor.
options->get_DigitalSignatureDetails()->set_TimestampSettings(
    MakeObject<PdfDigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword", System::TimeSpan::FromMinutes(30)));

ASPOSE_ASSERT_EQ(1800.0, options->get_DigitalSignatureDetails()->get_TimestampSettings()->get_Timeout().get_TotalSeconds());
ASSERT_EQ(u"https://freetsa.org/tsr", options->get_DigitalSignatureDetails()->get_TimestampSettings()->get_ServerUrl());
ASSERT_EQ(u"JohnDoe", options->get_DigitalSignatureDetails()->get_TimestampSettings()->get_UserName());
ASSERT_EQ(u"MyPassword", options->get_DigitalSignatureDetails()->get_TimestampSettings()->get_Password());

// The "Save" method will apply our signature to the output document at this time.
doc->Save(ArtifactsDir + u"PdfSaveOptions.PdfDigitalSignatureTimestamp.pdf", options);
```

## See Also

* Class [PdfDigitalSignatureTimestampSettings](../../pdfdigitalsignaturetimestampsettings/)
* Class [PdfDigitalSignatureDetails](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
