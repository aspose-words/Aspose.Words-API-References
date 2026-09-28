---
title: "Перечисление Aspose::Words::DigitalSignatures::XmlDsigLevel"
linktitle: "XmlDsigLevel"
second_title: "Справочник API Aspose.Words для C++"
description: "Перечисление Aspose::Words::DigitalSignatures::XmlDsigLevel. Указывает уровень цифровой подписи, основанный на стандарте XML-DSig в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enum


Указывает уровень цифровой подписи, основанный на стандарте XML-DSig.

```cpp
enum class XmlDsigLevel
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| XmlDSig | 0 | Указывает уровень подписи XML-DSig. |
| XAdEsEpes | 1 | Указывает уровень подписи XAdES-EPES. |


## Примеры



Показывает, как подписать документ на основе стандарта XML-DSig.
```cpp
System::SharedPtr<Aspose::Words::DigitalSignatures::CertificateHolder> certificateHolder = Aspose::Words::DigitalSignatures::CertificateHolder::Create(get_MyDir() + u"morzal.pfx", u"aw");
auto signOptions = System::MakeObject<Aspose::Words::DigitalSignatures::SignOptions>();
signOptions->set_XmlDsigLevel(Aspose::Words::DigitalSignatures::XmlDsigLevel::XAdEsEpes);

System::String inputFileName = get_MyDir() + u"Document.docx";
System::String outputFileName = get_ArtifactsDir() + u"DigitalSignatureUtil.XmlDsig.docx";
Aspose::Words::DigitalSignatures::DigitalSignatureUtil::Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

## См. также

* Namespace [Aspose::Words::DigitalSignatures](../)
* Library [Aspose.Words for C++](../../)
