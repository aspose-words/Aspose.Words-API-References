---
title: SignatureLine.ProviderId
linktitle: ProviderId
articleTitle: ProviderId
second_title: 用于 .NET 的 Aspose.Words
description: SignatureLine ProviderId 财产. 获取或设置此签名行的签名提供程序标识符 默认值为00000000000000000000000000000000 在 C#.
type: docs
weight: 80
url: /zh/net/aspose.words.drawing/signatureline/providerid/
---
## SignatureLine.ProviderId property

获取或设置此签名行的签名提供程序标识符。 默认值为“{00000000-0000-0000-0000-000000000000}”。

```csharp
public Guid ProviderId { get; set; }
```

## 评论

加密服务提供程序 (CSP) 是一个独立的软件模块，实际上执行用于身份验证、编码和加密的 加密算法。 MS Office 为其默认签名提供程序保留值 {00000000-0000-0000-0000-000000000000}。

额外安装的提供程序的 GUID 应从提供程序随附的文档中获取。

另外，所有已安装的加密提供程序都在Windows注册表中枚举。 可以在以下路径中找到：HKLM\SOFTWARE\Microsoft\Cryptography\Defaults\Provider。 有一个键名“CP Service UUID”，对应于签名提供者的 GUID。

## 例子

演示如何使用个人证书和签名行签署文档。

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

// 重新打开我们保存的文档，并验证“IsSigned”和“IsValid”属性都等于“true”，
// 表示签名行包含签名。
doc = new Document(ArtifactsDir + "DocumentBuilder.SignatureLineProviderId.Signed.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
signatureLine = shape.SignatureLine;

Assert.True(signatureLine.IsSigned);
Assert.True(signatureLine.IsValid);
```

### 也可以看看

* class [SignatureLine](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
