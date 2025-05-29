---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words для .NET
description: Откройте для себя свойство XmlDsigLevel в SignOptions, определяющее силу цифровой подписи по стандартам XMLDSig. Обеспечьте безопасные и надежные подписи!
type: docs
weight: 80
url: /ru/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

Указывает уровень цифровой подписи на основе стандарта XML-DSig. Значение по умолчанию:XmlDSig .

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## Примечания

Различные уровни подписей XAdES могут быть созданы, начиная с Office 2010.

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* пространство имен [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* сборка [Aspose.Words](../../../)
