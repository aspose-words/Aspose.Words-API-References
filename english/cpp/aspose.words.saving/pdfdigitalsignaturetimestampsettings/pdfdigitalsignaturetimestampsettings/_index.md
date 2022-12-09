---
title: PdfDigitalSignatureTimestampSettings
second_title: Aspose.Words for C++ API Reference
description: Initializes an instance of this class.
type: docs
weight: 14
url: /cpp/aspose.words.saving/pdfdigitalsignaturetimestampsettings/pdfdigitalsignaturetimestampsettings/
---
## PdfDigitalSignatureTimestampSettings::PdfDigitalSignatureTimestampSettings() constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::PdfDigitalSignatureTimestampSettings()
```

## See Also

* Class [PdfDigitalSignatureTimestampSettings](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
## PdfDigitalSignatureTimestampSettings::PdfDigitalSignatureTimestampSettings(const System::String\&, const System::String\&, const System::String\&) constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::PdfDigitalSignatureTimestampSettings(const System::String &serverUrl, const System::String &userName, const System::String &password)
```


| Parameter | Type | Description |
| --- | --- | --- |
| serverUrl | const System::String\& | Timestamp server URL. |
| userName | const System::String\& | Timestamp server user name. |
| password | const System::String\& | Timestamp server password. |

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

* Class [PdfDigitalSignatureTimestampSettings](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
## PdfDigitalSignatureTimestampSettings::PdfDigitalSignatureTimestampSettings(const System::String\&, const System::String\&, const System::String\&, System::TimeSpan) constructor


Initializes an instance of this class.

```cpp
Aspose::Words::Saving::PdfDigitalSignatureTimestampSettings::PdfDigitalSignatureTimestampSettings(const System::String &serverUrl, const System::String &userName, const System::String &password, System::TimeSpan timeout)
```


| Parameter | Type | Description |
| --- | --- | --- |
| serverUrl | const System::String\& | Timestamp server URL. |
| userName | const System::String\& | Timestamp server user name. |
| password | const System::String\& | Timestamp server password. |
| timeout | System::TimeSpan | Time-out value for accessing timestamp server. |

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

* Class [PdfDigitalSignatureTimestampSettings](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
