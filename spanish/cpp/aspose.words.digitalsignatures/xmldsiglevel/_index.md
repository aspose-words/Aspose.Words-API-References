---
title: "Aspose::Words::DigitalSignatures::XmlDsigLevel enumeración"
linktitle: "XmlDsigLevel"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::DigitalSignatures::XmlDsigLevel enumeración. Especifica el nivel de una firma digital basado en el estándar XML-DSig en C++."
type: docs
weight: 7000
url: /es/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Especifica el nivel de una firma digital basado en el estándar XML-DSig.

```cpp
enum class XmlDsigLevel
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| XmlDSig | 0 | Especifica el nivel de firma XML-DSig. |
| XAdEsEpes | 1 | Especifica el nivel de firma XAdES-EPES. |


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

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
