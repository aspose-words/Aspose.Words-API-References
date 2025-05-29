---
title: SignOptions.SignTime
linktitle: SignTime
articleTitle: SignTime
second_title: Aspose.Words for .NET
description: 探索 SignOptions SignTime，轻松签名。轻松设置签名日期，默认为当前时间。简化您的文档流程！
type: docs
weight: 70
url: /zh/net/aspose.words.digitalsignatures/signoptions/signtime/
---
## SignOptions.SignTime property

签署日期。 默认值为**当前时间**(Now)

```csharp
public DateTime SignTime { get; set; }
```

## 例子

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储区创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建将与我们的新数字签名一起应用的评论和日期。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统获取未签名的文档，
// 然后根据输出文件流的文件名创建它的签名副本。
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
