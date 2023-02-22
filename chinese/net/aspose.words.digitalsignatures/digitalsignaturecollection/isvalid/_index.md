---
title: DigitalSignatureCollection.IsValid
second_title: Aspose.Words for .NET API 参考
description: DigitalSignatureCollection 财产. 返回真的如果这个集合中的所有数字签名都有效并且文档没有被篡改 也返回真的如果没有数字签名 返回错误的如果至少一个数字签名无效
type: docs
weight: 30
url: /zh/net/aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/
---
## DigitalSignatureCollection.IsValid property

返回`真的`如果这个集合中的所有数字签名都有效并且文档没有被篡改 也返回`真的`如果没有数字签名。 返回`错误的`如果至少一个数字签名无效。

```csharp
public bool IsValid { get; }
```

### 例子

显示如何使用 X.509 证书签署文档。

```csharp
// 验证文档是否未签名。
Assert.False(FileFormatUtil.DetectFileFormat(MyDir + "Document.docx").HasDigitalSignature);

// 从 PKCS12 文件创建一个 CertificateHolder 对象，我们将使用它来签署文档。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw", null);

// 将文档的签名副本保存到本地文件系统有两种方法：
// 1 - 通过本地系统文件名指定一个文档，并将签名副本保存在另一个文件名指定的位置。
DigitalSignatureUtil.Sign(MyDir + "Document.docx", ArtifactsDir + "Document.DigitalSignature.docx", 
    certificateHolder, new SignOptions() { SignTime = DateTime.Now } );

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 2 - 从流中获取文档并将签名副本保存到另一个流。
using (FileStream inDoc = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (FileStream outDoc = new FileStream(ArtifactsDir + "Document.DigitalSignature.docx", FileMode.Create))
    {
        DigitalSignatureUtil.Sign(inDoc, outDoc, certificateHolder);
    }
}

Assert.True(FileFormatUtil.DetectFileFormat(ArtifactsDir + "Document.DigitalSignature.docx").HasDigitalSignature);

// 请验证文档的所有数字签名是否有效并检查其详细信息。
Document signedDoc = new Document(ArtifactsDir + "Document.DigitalSignature.docx");
DigitalSignatureCollection digitalSignatureCollection = signedDoc.DigitalSignatures;

Assert.True(digitalSignatureCollection.IsValid);
Assert.AreEqual(1, digitalSignatureCollection.Count);
Assert.AreEqual(DigitalSignatureType.XmlDsig, digitalSignatureCollection[0].SignatureType);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].IssuerName);
Assert.AreEqual("CN=Morzal.Me", signedDoc.DigitalSignatures[0].SubjectName);
```

### 也可以看看

* class [DigitalSignatureCollection](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignaturecollection/)
* 部件 [Aspose.Words](../../../)


