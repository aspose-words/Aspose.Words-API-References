---
title: SignOptions.XmlDsigLevel
linktitle: XmlDsigLevel
articleTitle: XmlDsigLevel
second_title: Aspose.Words for .NET
description: 探索 SignOptions 中的 XmlDsigLevel 属性，根据 XMLDSig 标准定义数字签名强度。确保签名安全可靠！
type: docs
weight: 80
url: /zh/net/aspose.words.digitalsignatures/signoptions/xmldsiglevel/
---
## SignOptions.XmlDsigLevel property

指定基于 XML-DSig 标准的数字签名级别。 默认值为XmlDSig.

```csharp
public XmlDsigLevel XmlDsigLevel { get; set; }
```

## 评论

从 Office 2010 开始可以创建不同级别的 XAdES 签名。

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

* enum [XmlDsigLevel](../../xmldsiglevel/)
* class [SignOptions](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
