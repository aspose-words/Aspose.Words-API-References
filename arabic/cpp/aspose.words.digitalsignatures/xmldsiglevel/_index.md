---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum"
linktitle: "XmlDsigLevel"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum. يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig في C++."
type: docs
weight: 7000
url: /ar/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


يحدد مستوى التوقيع الرقمي بناءً على معيار XML-DSig.

```cpp
enum class XmlDsigLevel
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| XmlDSig | 0 | يحدد مستوى توقيع XML-DSig. |
| XAdEsEpes | 1 | يحدد مستوى توقيع XAdES-EPES. |


## أمثلة



يعرض كيفية توقيع المستند بناءً على معيار XML-DSig.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## انظر أيضًا

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
