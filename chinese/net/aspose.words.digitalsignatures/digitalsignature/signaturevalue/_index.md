---
title: DigitalSignature.SignatureValue
second_title: Aspose.Words for .NET API 参考
description: DigitalSignature 财产. 获取表示签名值的字节数组
type: docs
weight: 60
url: /zh/net/aspose.words.digitalsignatures/digitalsignature/signaturevalue/
---
## DigitalSignature.SignatureValue property

获取表示签名值的字节数组。

```csharp
public byte[] SignatureValue { get; }
```

### 例子

演示如何从数字签名文档中获取数字签名值。

```csharp
Document doc = new Document(MyDir + "Digitally signed.docx");

foreach (DigitalSignature digitalSignature in doc.DigitalSignatures)
{
    string signatureValue = Convert.ToBase64String(digitalSignature.SignatureValue);
    Assert.AreEqual("K1cVLLg2kbJRAzT5WK+m++G8eEO+l7S+5ENdjMxxTXkFzGUfvwxREuJdSFj9AbD" +
        "MhnGvDURv9KEhC25DDF1al8NRVR71TF3CjHVZXpYu7edQS5/yLw/k5CiFZzCp1+MmhOdYPcVO+Fm" +
        "+9fKr2iNLeyYB+fgEeZHfTqTFM2WwAqo=", signatureValue);
}
```

### 也可以看看

* class [DigitalSignature](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../digitalsignature/)
* 部件 [Aspose.Words](../../../)


