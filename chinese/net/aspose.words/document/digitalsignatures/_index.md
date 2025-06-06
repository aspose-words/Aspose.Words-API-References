---
title: Document.DigitalSignatures
linktitle: DigitalSignatures
articleTitle: DigitalSignatures
second_title: Aspose.Words for .NET
description: 探索 DigitalSignatures 属性，轻松访问和验证文档的数字签名。轻松确保真实性和安全性。
type: docs
weight: 110
url: /zh/net/aspose.words/document/digitalsignatures/
---
## Document.DigitalSignatures property

获取此文档的数字签名集合及其验证结果。

```csharp
public DigitalSignatureCollection DigitalSignatures { get; }
```

## 评论

此集合包含从原始文档加载的数字签名。 保存此文件时，这些数字签名将不会被保存[`Document`](../)object 放入文件或流中，因为保存或转换将生成与原始文档不同的文档，并且原始数字签名将不再有效。

此系列从不`无效的`。如果该文件未签名，则它将包含零个元素。

## 例子

展示如何验证和显示文档中每个签名的信息。

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature signature in doc.DigitalSignatures)
{
    Console.WriteLine($"{(signature.IsValid ? "Valid" : "Invalid")} signature: ");
    Console.WriteLine($"\tReason:\t{signature.Comments}");
    Console.WriteLine($"\tType:\t{signature.SignatureType}");
    Console.WriteLine($"\tSign time:\t{signature.SignTime}");
    Console.WriteLine($"\tSubject name:\t{signature.CertificateHolder.Certificate.SubjectName}");
    Console.WriteLine($"\tIssuer name:\t{signature.CertificateHolder.Certificate.IssuerName.Name}");
    Console.WriteLine();
}
```

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

* class [DigitalSignatureCollection](../../../aspose.words.digitalsignatures/digitalsignaturecollection/)
* class [Document](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
