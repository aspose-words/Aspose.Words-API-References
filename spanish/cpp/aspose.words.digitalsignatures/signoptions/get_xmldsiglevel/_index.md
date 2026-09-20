---
title: "Método Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel"
linktitle: "get_XmlDsigLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Método Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel. Especifica el nivel de una firma digital basado en el estándar XML-DSig. El valor predeterminado es XmlDSig en C++."
type: docs
weight: 8500
url: /es/cpp/aspose.words.digitalsignatures/signoptions/get_xmldsiglevel/
---
## SignOptions::get_XmlDsigLevel method


Especifica el nivel de una firma digital basado en el estándar XML-DSig. El valor predeterminado es [XmlDSig](../../xmldsiglevel/).

```cpp
Aspose::Words::DigitalSignatures::XmlDsigLevel Aspose::Words::DigitalSignatures::SignOptions::get_XmlDsigLevel() const
```


## Ejemplos



Muestra cómo firmar un documento basado en el estándar XML-DSig.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## Ver también

* Enum [XmlDsigLevel](../../xmldsiglevel/)
* Class [SignOptions](../)
* Namespace [Aspose::Words::DigitalSignatures](../../)
* Library [Aspose.Words for C++](../../../)
