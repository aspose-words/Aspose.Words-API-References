---
title: Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings class
linktitle: DigitalSignatureTimestampSettings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings class. Contains settings of the digital signature timestamp in C++.'
type: docs
weight: 3500
url: /cpp/aspose.words.digitalsignatures/digitalsignaturetimestampsettings/
---
## DigitalSignatureTimestampSettings class


Contains settings of the digital signature timestamp.

```cpp
class DigitalSignatureTimestampSettings : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [DigitalSignatureTimestampSettings](./digitalsignaturetimestampsettings/)() | Initializes a new instance of [DigitalSignatureTimestampSettings](./) class. |
| [DigitalSignatureTimestampSettings](./digitalsignaturetimestampsettings/)(const System::String\&, const System::String\&, const System::String\&) | Initializes a new instance of [DigitalSignatureTimestampSettings](./) class. |
| [DigitalSignatureTimestampSettings](./digitalsignaturetimestampsettings/)(const System::String\&, const System::String\&, const System::String\&, System::TimeSpan) | Initializes a new instance of [DigitalSignatureTimestampSettings](./) class. |
| [get_Password](./get_password/)() const | Gets or sets a string value representing timestamp server password. The default value is **null**. |
| [get_ServerUrl](./get_serverurl/)() const | Gets or sets a string value representing timestamp server URL. The default value is **null**. |
| [get_Timeout](./get_timeout/)() const | Gets or sets a time-out value for accessing timestamp server. The default value is 100 seconds. |
| [get_UserName](./get_username/)() const | Gets or sets a string value representing timestamp server user name. The default value is **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Password](./set_password/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_Password](./get_password/). |
| [set_ServerUrl](./set_serverurl/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_ServerUrl](./get_serverurl/). |
| [set_Timeout](./set_timeout/)(System::TimeSpan) | Setter for [Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_Timeout](./get_timeout/). |
| [set_UserName](./set_username/)(const System::String\&) | Setter for [Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_UserName](./get_username/). |
| static [Type](./type/)() |  |

## Examples



Shows how to sign a document with timestamping using [DigitalSignatureUtil](../digitalsignatureutil/). 
```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(XmlDsigLevel::XAdEsT);
signOptions->set_TimestampSettings(System::MakeObject<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword"));

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"DigitalSignatureUtil.Timestamped.docx"));

ASSERT_EQ(1, signedDoc->get_DigitalSignatures()->get_Count());
ASSERT_TRUE(signedDoc->get_DigitalSignatures()->idx_get(0)->get_IsValid());

// Verify timestamp settings are applied.
ASSERT_EQ(u"https://freetsa.org/tsr", signOptions->get_TimestampSettings()->get_ServerUrl());
ASSERT_EQ(u"JohnDoe", signOptions->get_TimestampSettings()->get_UserName());
ASSERT_EQ(u"MyPassword", signOptions->get_TimestampSettings()->get_Password());
ASPOSE_ASSERT_EQ(100.0, signOptions->get_TimestampSettings()->get_Timeout().get_TotalSeconds());

// Test with custom timeout.
signOptions->set_TimestampSettings(System::MakeObject<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword", System::TimeSpan::FromMinutes(30)));

ASPOSE_ASSERT_EQ(1800.0, signOptions->get_TimestampSettings()->get_Timeout().get_TotalSeconds());
```

## See Also

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
