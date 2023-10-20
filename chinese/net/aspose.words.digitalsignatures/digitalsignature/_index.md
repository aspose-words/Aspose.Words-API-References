---
title: DigitalSignature Class
linktitle: DigitalSignature
articleTitle: DigitalSignature
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.DigitalSignatures.DigitalSignature 班级. 表示文档上的数字签名及其验证结果 在 C#.
type: docs
weight: 380
url: /zh/net/aspose.words.digitalsignatures/digitalsignature/
---
## DigitalSignature class

表示文档上的数字签名及其验证结果。

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public class DigitalSignature
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [CertificateHolder](../../aspose.words.digitalsignatures/digitalsignature/certificateholder/) { get; } | 返回包含用于签署文档的证书的证书持有者对象。 |
| [Comments](../../aspose.words.digitalsignatures/digitalsignature/comments/) { get; } | 获取签名目的注释。 |
| [IssuerName](../../aspose.words.digitalsignatures/digitalsignature/issuername/) { get; } | 返回证书 isuuer 的主题专有名称。 |
| [IsValid](../../aspose.words.digitalsignatures/digitalsignature/isvalid/) { get; } | 返回`真的`如果此数字签名有效且文档未被篡改。 |
| [SignatureType](../../aspose.words.digitalsignatures/digitalsignature/signaturetype/) { get; } | 获取数字签名的类型。 |
| [SignatureValue](../../aspose.words.digitalsignatures/digitalsignature/signaturevalue/) { get; } | 获取表示签名值的字节数组。 |
| [SignTime](../../aspose.words.digitalsignatures/digitalsignature/signtime/) { get; } | 获取文档的签名时间。 |
| [SubjectName](../../aspose.words.digitalsignatures/digitalsignature/subjectname/) { get; } | 返回用于签署文档的证书的主题可分辨名称。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [ToString](../../aspose.words.digitalsignatures/digitalsignature/tostring/)() | 返回一个用户友好的字符串，显示该对象的值。 |

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

* 命名空间 [Aspose.Words.DigitalSignatures](../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../)
