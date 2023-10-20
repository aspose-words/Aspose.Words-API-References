---
title: DigitalSignatureCollection Class
linktitle: DigitalSignatureCollection
articleTitle: DigitalSignatureCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.DigitalSignatures.DigitalSignatureCollection 班级. 提供附加到文档的数字签名的只读集合 在 C#.
type: docs
weight: 390
url: /zh/net/aspose.words.digitalsignatures/digitalsignaturecollection/
---
## DigitalSignatureCollection class

提供附加到文档的数字签名的只读集合。

```csharp
public class DigitalSignatureCollection : IEnumerable<DigitalSignature>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [DigitalSignatureCollection](digitalsignaturecollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.digitalsignatures/digitalsignaturecollection/count/) { get; } | 获取集合中包含的元素数。 |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignaturecollection/isvalid/) { get; } | 返回`真的`如果这个集合中的所有数字签名都有效并且文档没有被篡改 也返回`真的`如果没有数字签名。 返回`错误的`如果至少一个数字签名无效。 |
| [Item](../../aspose.words.digitalsignatures/digitalsignaturecollection/item/) { get; } | 获取指定索引处的文档签名。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.digitalsignatures/digitalsignaturecollection/getenumerator/)() | 返回一个字典枚举器对象，可用于迭代集合中的所有项目。 |

## 评论

[`DigitalSignatures`](../../aspose.words/document/digitalsignatures/)

## 例子

演示如何验证和显示有关文档中每个签名的信息。

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

* class [DigitalSignature](../digitalsignature/)
* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
