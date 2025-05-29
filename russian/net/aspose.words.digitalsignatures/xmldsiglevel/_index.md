---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words для .NET
description: Изучите перечисление Aspose.Words.DigitalSignatures.XmlDsigLevel, чтобы улучшить свои цифровые подписи с помощью стандартов XMLDSig для обеспечения безопасной и надежной целостности документов.
type: docs
weight: 630
url: /ru/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

Указывает уровень цифровой подписи на основе стандарта XML-DSig.

```csharp
public enum XmlDsigLevel
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| XmlDSig | `0` | Указывает уровень подписи XML-DSig. |
| XAdEsEpes | `1` | Указывает уровень подписи XAdES-EPES. |

## Примеры

Показывает, как подписывать документы на основе стандарта XML-DSig.

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### Смотрите также

* пространство имен [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../)
