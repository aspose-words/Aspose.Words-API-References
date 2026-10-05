---
title: Aspose::Words::DigitalSignatures::SignOptions::get_TimestampSettings method
linktitle: get_TimestampSettings
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DigitalSignatures::SignOptions::get_TimestampSettings method. Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA). The default value is null and the digital signature will not be time-stamped in C++.'
type: docs
weight: 8084
url: /cpp/aspose.words.digitalsignatures/signoptions/get_timestampsettings/
---
## SignOptions::get_TimestampSettings method


Specifies settings for timestamping the digital signature using an RFC 3161 timestamp authority (TSA). The default value is **null** and the digital signature will not be time-stamped.

```cpp
const System::SharedPtr<Aspose::Words::DigitalSignatures::DigitalSignatureTimestampSettings> & Aspose::Words::DigitalSignatures::SignOptions::get_TimestampSettings() const
```


## Examples



Shows how to sign a document with timestamping using [DigitalSignatureUtil](../../digitalsignatureutil/). 
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

* Class [DigitalSignatureTimestampSettings](../../digitalsignaturetimestampsettings/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
