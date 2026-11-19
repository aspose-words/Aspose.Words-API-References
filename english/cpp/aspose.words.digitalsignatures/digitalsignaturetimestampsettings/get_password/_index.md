---
title: Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_Password method
linktitle: get_Password
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_Password method. Gets or sets a string value representing timestamp server password. The default value is null in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.digitalsignatures/digitalsignaturetimestampsettings/get_password/
---
## DigitalSignatureTimestampSettings::get_Password method


Gets or sets a string value representing timestamp server password. The default value is **null**.

```cpp
System::String Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings::get_Password() const
```

## Remarks

## Examples


Shows how to sign a document with timestamping using [DigitalSignatureUtil](../../digitalsignatureutil/).

```cpp
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(XmlDsigLevel::XAdEsT);
signOptions->set_TimestampSettings(System::MakeObject<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword"));

System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> cert = CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");

DigitalSignatureUtil::Sign(get_MyDir() + u"Digitally signed.docx", get_ArtifactsDir() + u"DigitalSignatureUtil.Timestamped.docx", cert, signOptions);

auto signedDoc = System::MakeObject<Aspose::Words::Document>(System::String(get_ArtifactsDir() + u"DigitalSignatureUtil.Timestamped.docx"));

ASSERT_EQ(signedDoc->get_DigitalSignatures()->get_Count(), 1);
ASSERT_TRUE(signedDoc->get_DigitalSignatures()->idx_get(0)->get_IsValid());

// Verify timestamp settings are applied.
ASSERT_EQ(signOptions->get_TimestampSettings()->get_ServerUrl(), u"https://freetsa.org/tsr");
ASSERT_EQ(signOptions->get_TimestampSettings()->get_UserName(), u"JohnDoe");
ASSERT_EQ(signOptions->get_TimestampSettings()->get_Password(), u"MyPassword");
ASPOSE_ASSERT_EQ(signOptions->get_TimestampSettings()->get_Timeout().get_TotalSeconds(), 100.0);

// Test with custom timeout.
signOptions->set_TimestampSettings(System::MakeObject<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings>(u"https://freetsa.org/tsr", u"JohnDoe", u"MyPassword", System::TimeSpan::FromMinutes(30)));

ASPOSE_ASSERT_EQ(signOptions->get_TimestampSettings()->get_Timeout().get_TotalSeconds(), 1800.0);
```
## See Also

* Class [DigitalSignatureTimestampSettings](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
