---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum"
linktitle: "XmlDsigLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel enum. Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig en C++."
type: docs
weight: 7000
url: /fr/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig.

```cpp
enum class XmlDsigLevel
```

### Valeurs

| Nom | Valeur | Description |
| --- | --- | --- |
| XmlDSig | 0 | Spécifie le niveau de la signature XML-DSig. |
| XAdEsEpes | 1 | Spécifie le niveau de la signature XAdES-EPES. |


## Exemples



Montre comment signer un document basé sur la norme XML-DSig.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Voir aussi

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
