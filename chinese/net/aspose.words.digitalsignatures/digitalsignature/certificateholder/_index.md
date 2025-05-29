---
title: DigitalSignature.CertificateHolder
linktitle: CertificateHolder
articleTitle: CertificateHolder
second_title: Aspose.Words for .NET
description: 发现 DigitalSignature CertificateHolder 属性，该属性检索证书持有者对象以增强文档签名安全性和验证。
type: docs
weight: 10
url: /zh/net/aspose.words.digitalsignatures/digitalsignature/certificateholder/
---
## DigitalSignature.CertificateHolder property

返回包含用于签署文档的证书的证书持有者对象。

```csharp
public CertificateHolder CertificateHolder { get; }
```

## 例子

展示如何使用 X.509 证书签署文档。

```csharp
// 验证文档未签名。
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// 从 PKCS12 文件创建一个 CertificateHolder 对象，我们将使用它来签署文档。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// 有两种方法可以将文档的签名副本保存到本地文件系统：
// 1 - 通过本地系统文件名指定文档，并将签名副本保存在另一个文件名指定的位置。
SignOptions signOptions = new SignOptions { SignTime = DateTime.Now };
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx",
    certificateHolder, signOptions);

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - 从流中获取文档并将签名的副本保存到另一个流。
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 请验证所有文档的数字签名是否有效并检查其详细信息。
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### 也可以看看

* class [CertificateHolder](../../certificateholder/)
* class [DigitalSignature](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
