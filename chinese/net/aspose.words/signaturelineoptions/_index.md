---
title: SignatureLineOptions Class
linktitle: SignatureLineOptions
articleTitle: SignatureLineOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.SignatureLineOptions，轻松自定义文档中的签名行。立即提升您的 DocumentBuilder 体验！
type: docs
weight: 6940
url: /zh/net/aspose.words/signaturelineoptions/
---
## SignatureLineOptions class

允许指定插入签名行的选项。用于[`DocumentBuilder`](../documentbuilder/).

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public class SignatureLineOptions
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [SignatureLineOptions](signaturelineoptions/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowComments](../../aspose.words/signaturelineoptions/allowcomments/) { get; set; } | 获取或设置一个值，表示签名者可以在签名对话框中添加注释。 此属性的默认值为`错误的`. |
| [DefaultInstructions](../../aspose.words/signaturelineoptions/defaultinstructions/) { get; set; } | 获取或设置一个值，指示在签名对话框中显示默认说明。 此属性的默认值为`真的`. |
| [Email](../../aspose.words/signaturelineoptions/email/) { get; set; } | 获取或设置建议签名者的电子邮件地址。 此属性的默认值为**空字符串**(Empty ). |
| [Instructions](../../aspose.words/signaturelineoptions/instructions/) { get; set; } | 获取或设置在签署签名行时显示的签名者指示。 此属性的默认值为**空字符串**(Empty ). |
| [ShowDate](../../aspose.words/signaturelineoptions/showdate/) { get; set; } | 获取或设置一个值，指示签名行中显示签名日期。 此属性的默认值为`真的`. |
| [Signer](../../aspose.words/signaturelineoptions/signer/) { get; set; } | 获取或设置签名行的建议签名者。 此属性的默认值为**空字符串**(Empty ). |
| [SignerTitle](../../aspose.words/signaturelineoptions/signertitle/) { get; set; } | 获取或设置建议签名者的职称。 此属性的默认值为**空字符串**(Empty ). |

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

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
