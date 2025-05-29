---
title: DigitalSignature.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words for .NET
description: 探索“数字签名注释”功能，通过清晰的注释增强您的签名流程。提升文档的效率和清晰度！
type: docs
weight: 20
url: /zh/net/aspose.words.digitalsignatures/digitalsignature/comments/
---
## DigitalSignature.Comments property

获取签名目的注释。

```csharp
public string Comments { get; }
```

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

### 也可以看看

* class [DigitalSignature](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
