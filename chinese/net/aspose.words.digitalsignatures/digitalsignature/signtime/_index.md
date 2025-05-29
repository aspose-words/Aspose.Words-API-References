---
title: DigitalSignature.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: Aspose.Words for .NET
description: 探索 DigitalSignature SignTime。追踪文档签署的准确时间，增强安全性并提高记录保存效率。
type: docs
weight: 70
url: /zh/net/aspose.words.digitalsignatures/digitalsignature/signtime/
---
## DigitalSignature.SignTime property

获取文件签署的时间。

```csharp
public DateTime SignTime { get; }
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
