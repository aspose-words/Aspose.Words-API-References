---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: 用于 .NET 的 Aspose.Words
description: SignOptions SignTime 财产. 签署日期 默认值为当前时间Now  在 C#.
type: docs
weight: 70
url: /zh/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

签署日期。 默认值为**当前时间**(Now ).

```csharp
public DateTime SignTime { get; set; }
```

## 例子

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储创建 X.509 证书，其中应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建一个评论和日期，它将与我们的新数字签名一起应用。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统中获取未签名的文档，
// 然后创建一个由输出文件流的文件名确定的签名副本。
using (Stream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open))
{
    using (Stream streamOut = new FileStream(ArtifactsDir + "DigitalSignatureUtil.SignDocument.docx", FileMode.OpenOrCreate))
    {
        DigitalSignatureUtil.Sign(streamIn, streamOut, certificateHolder, signOptions);
    }
}
```

### 也可以看看

* class [SignOptions](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
