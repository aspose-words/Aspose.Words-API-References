---
title: DocumentBuilder.InsertSignatureLine
linktitle: InsertSignatureLine
articleTitle: InsertSignatureLine
second_title: 用于 .NET 的 Aspose.Words
description: DocumentBuilder InsertSignatureLine 方法. 在当前位置插入签名行 在 C#.
type: docs
weight: 440
url: /zh/net/aspose.words/documentbuilder/insertsignatureline/
---
## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/)*) {#insertsignatureline}

在当前位置插入签名行。

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | 存储创建签名行参数的对象。 |

### 返回值

刚刚插入的签名行节点。

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

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## InsertSignatureLine(*[SignatureLineOptions](../../signaturelineoptions/), [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertsignatureline_1}

在指定位置插入签名行。

```csharp
public Shape InsertSignatureLine(SignatureLineOptions signatureLineOptions, 
    RelativeHorizontalPosition horzPos, double left, RelativeVerticalPosition vertPos, double top, 
    WrapType wrapType)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| signatureLineOptions | SignatureLineOptions | 存储创建签名行参数的对象。 |
| horzPos | RelativeHorizontalPosition | 指定从何处测量到签名线的距离。 |
| left | Double | 从原点到签名线左侧的距离（以磅为单位）。 |
| vertPos | RelativeVerticalPosition | 指定从何处测量到签名线的距离。 |
| top | Double | 从原点到签名线顶边的距离（以磅为单位）。 |
| wrapType | WrapType | 指定如何将文本环绕签名行。 |

### 返回值

刚刚插入的签名行节点。

## 评论

您可以使用 更改图像大小、位置、定位方法和其他设置[`Shape`](../../../aspose.words.drawing/shape/)该方法返回的对象。

## 例子

演示如何将内嵌签名行插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    Signer = "John Doe",
    SignerTitle = "Manager",
    Email = "johndoe@aspose.com",
    ShowDate = true,
    DefaultInstructions = false,
    Instructions = "Please sign here.",
    AllowComments = true
};

builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, 2.0,
    RelativeVerticalPosition.Page, 3.0, WrapType.Inline);

// 签名行可以在 Microsoft Word 中双击签名。
doc.Save(ArtifactsDir + "DocumentBuilder.SignatureLineInline.docx");
```

### 也可以看看

* class [Shape](../../../aspose.words.drawing/shape/)
* class [SignatureLineOptions](../../signaturelineoptions/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
