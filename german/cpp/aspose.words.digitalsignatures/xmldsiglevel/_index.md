---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel Aufzählung"
linktitle: "XmlDsigLevel"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel Aufzählung. Gibt das Niveau einer digitalen Signatur basierend auf dem XML-DSig-Standard in C++ an."
type: docs
weight: 7000
url: /de/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Gibt das Niveau einer digitalen Signatur basierend auf dem XML-DSig-Standard an.

```cpp
enum class XmlDsigLevel
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| XmlDSig | 0 | Gibt das XML-DSig-Signaturniveau an. |
| XAdEsEpes | 1 | Gibt das XAdES-EPES-Signaturniveau an. |


## Beispiele



Zeigt, wie man ein Dokument basierend auf dem XML-DSig-Standard signiert.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Siehe auch

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
