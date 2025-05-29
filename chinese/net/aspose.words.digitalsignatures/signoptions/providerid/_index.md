---
title: SignOptions.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: Aspose.Words for .NET
description: 探索 SignOptions ProviderId 属性，定义签名提供商的类 ID。轻松使用唯一的 GUID 进行自定义，以获得最佳性能。
type: docs
weight: 40
url: /zh/net/aspose.words.digitalsignatures/signoptions/providerid/
---
## SignOptions.ProviderId property

指定签名提供者的类 ID。 默认值为**空（全零）Guid**.

```csharp
public Guid ProviderId { get; set; }
```

## 评论

加密服务提供程序 (CSP) 是一个独立的软件模块，它实际上执行用于身份验证、编码和加密的加密算法。MS Office 为其默认签名提供程序保留了 {00000000-0000-0000-0000-00000000000} 的值。

应从提供程序附带的文档中获取附加安装的提供程序的 GUID。

此外，所有已安装的加密提供程序都枚举在 Windows 注册表中。 它可以在以下路径中找到：HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider。 有一个名为“CP Service UUID”的键值，它对应于签名提供程序的 GUID。

## 例子

展示如何使用个人证书和签名行签署文件。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions signatureLineOptions = new SignatureLineOptions
{
    Signer = "vderyushev",
    SignerTitle = "QA",
    Email = "vderyushev@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

SignatureLine signatureLine = builder.InsertSignatureLine(signatureLineOptions).SignatureLine;
signatureLine.ProviderId = Guid.Parse("CF5A7BB4-8F3C-4756-9DF6-BEF7F13259A2");

Assert.False(signatureLine.IsSigned);
Assert.False(signatureLine.IsValid);

doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx");

SignOptions signOptions = new SignOptions
{
    SignatureLineId = signatureLine.Id,
    ProviderId = signatureLine.ProviderId,
    Comments = "Document was signed by vderyushev",
    SignTime = DateTime.Now
};

CertificateHolder certHolder = CertificateHolder.Create(MyDir + "morzal.pfx", "aw");

DigitalSignatureUtil.Sign(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.docx", 
    ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx", certHolder, signOptions);

// 重新打开我们保存的文档，并验证“IsSigned”和“IsValid”属性是否都等于“true”，
// 表示签名行包含签名。
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### 也可以看看

* class [SignOptions](../)
* 命名空间 [Aspose.Words.DigitalSignatures](../../../aspose.words.digitalsignatures/)
* 部件 [Aspose.Words](../../../)
