---
title: SignOptions.Comments
second_title: Aspose.Words for .NET API 参考
description: SignOptions 财产. 指定数字签名的注释 默认值为 空字符串Empty.
type: docs
weight: 20
url: /zh/net/aspose.words.digitalsignatures/signoptions/comments/
---
## SignOptions.Comments property

指定数字签名的注释。 默认值为 **空字符串**（Empty).

```csharp
public string Comments { get; set; }
```

### 例子

展示如何对文档进行数字签名。

```csharp
// 从 PKCS#12 存储创建 X.509 证书，该证书应包含私钥。
CertificateHolder certificateHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

// 创建评论和日期，该评论和日期将与我们的新数字签名一起应用。
SignOptions signOptions = new SignOptions
{
    Comments = "My comment", 
    SignTime = DateTime.Now
};

// 通过文件流从本地文件系统获取未签名的文档，
// 然后创建由输出文件流的文件名确定的签名副本。
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
* 命名空间 [Aspose.Words.DigitalSignatures](../../signoptions/)
* 部件 [Aspose.Words](../../../)


