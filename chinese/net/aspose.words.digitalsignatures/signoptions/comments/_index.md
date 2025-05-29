---
title: SignOptions.Comments
linktitle: Comments
articleTitle: Comments
second_title: Aspose.Words for .NET
description: 探索 SignOptions 的“注释”属性，使用自定义注释增强您的数字签名。轻松提升清晰度和沟通效果！
type: docs
weight: 20
url: /zh/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

指定数字签名的注释。 默认值为**空字符串**(Empty ).

```csharp
public string Comments { get; set; }
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
