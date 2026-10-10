---
title: "Méthode Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel"
linktitle: "get_XmlDsigLevel"
second_title: "Référence de l'API Aspose.Words pour C++"
description: "Méthode Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel. Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. La valeur par défaut est XmlDSig en C++."
type: docs
weight: 8500
url: /fr/cpp/aspose.words.digitalsignatures/signoptions/get_xmldsiglevel/
---
## SignOptions::get_XmlDsigLevel method


Spécifie le niveau d'une signature numérique basé sur la norme XML-DSig. La valeur par défaut est [XmlDSig](../../xmldsiglevel/).

```cpp
Aspose::Words::DigitalSignatures::XmlDsigLevel Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel() const
```


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

* Enum [XmlDsigLevel](../../xmldsiglevel/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
