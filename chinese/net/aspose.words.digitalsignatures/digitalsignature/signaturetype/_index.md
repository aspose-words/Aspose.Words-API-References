---
title: DigitalSignature.SignatureType
linktitle: SignatureType
articleTitle: SignatureType
second_title: 用于 .NET 的 Aspose.Words
description: DigitalSignature SignatureType 财产. 获取数字签名的类型 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words.digitalsignatures/digitalsignature/signaturetype/
---
## DigitalSignature.SignatureType property

获取数字签名的类型。

```csharp
public DigitalSignatureType SignatureType { get; }
```

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

* enum [DigitalSignatureType](../../digitalsignaturetype/)
* class [DigitalSignature](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
