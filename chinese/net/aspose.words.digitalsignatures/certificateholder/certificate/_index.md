---
title: CertificateHolder.Certificate
linktitle: Certificate
articleTitle: Certificate
second_title: 用于 .NET 的 Aspose.Words
description: CertificateHolder Certificate 财产. 返回以下实例X509证书2它保存私钥公钥和证书链 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.digitalsignatures/certificateholder/certificate/
---
## CertificateHolder.Certificate property

返回以下实例**X509证书2**它保存私钥、公钥和证书链。

```csharp
public X509Certificate2 Certificate { get; }
```

### 返回值

X509Certificate2实例

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

### 也可以看看

* class [CertificateHolder](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
