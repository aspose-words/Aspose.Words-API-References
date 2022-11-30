---
title: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words for C++ API Reference
description: Contains settings of the digital signature timestamp.
type: docs
weight: 287
url: /cpp/aspose.words.saving/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings class


Contains settings of the digital signature timestamp.

```cpp
class PdfDigitalSignatureTimestampSettings : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_Password](./get_password/)() const | Timestamp server password. |
| [get_ServerUrl](./get_serverurl/)() const | Timestamp server URL. |
| [get_Timeout](./get_timeout/)() const | Time-out value for accessing timestamp server. |
| [get_UserName](./get_username/)() const | Timestamp server user name. |
| [PdfDigitalSignatureTimestampSettings](./pdfdigitalsignaturetimestampsettings/)() | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings](./pdfdigitalsignaturetimestampsettings/)(const System::String\&, const System::String\&, const System::String\&) | Initializes an instance of this class. |
| [PdfDigitalSignatureTimestampSettings](./pdfdigitalsignaturetimestampsettings/)(const System::String\&, const System::String\&, const System::String\&, System::TimeSpan) | Initializes an instance of this class. |
| [set_Password](./set_password/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::get_Password](./get_password/). |
| [set_ServerUrl](./set_serverurl/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::get_ServerUrl](./get_serverurl/). |
| [set_Timeout](./set_timeout/)(System::TimeSpan) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::get_Timeout](./get_timeout/). |
| [set_UserName](./set_username/)(const System::String\&) | Setter for [Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::get_UserName](./get_username/). |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words](../../)
