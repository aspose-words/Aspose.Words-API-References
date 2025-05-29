---
title: XmlDsigLevel Enum
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.DigitalSignatures.XmlDsigLevel 枚举，以使用 XMLDSig 标准增强您的数字签名，从而实现安全可靠的文档完整性。
type: docs
weight: 630
url: /zh/net/aspose.words.digitalsignatures/xmldsiglevel/
---
## XmlDsigLevel enumeration

指定基于 XML-DSig 标准的数字签名级别。

```csharp
public enum XmlDsigLevel
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| XmlDSig | `0` | 指定 XML-DSig 签名级别。 |
| XAdEsEpes | `1` | 指定 XAdES-EPES 签名级别。 |

## 例子

展示如何基于 XML-DSig 标准签署文档。

```csharp
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");
SignOptions signOptions = new SignOptions { XmlDsigLevel = XmlDsigLevel.XAdEsEpes };

string inputFileName = MyDir + "Document.docx";
string outputFileName = ArtifactsDir + "DigitalSignatureUtil.XmlDsig.docx";
DigitalSignatureUtil.Sign(inputFileName, outputFileName, certificateHolder, signOptions);
```

### 也可以看看

* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
