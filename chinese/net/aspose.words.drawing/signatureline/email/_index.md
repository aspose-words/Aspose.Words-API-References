---
title: SignatureLine.Email
linktitle: Email
articleTitle: Email
second_title: Aspose.Words for .NET
description: 使用 SignatureLine 电子邮件属性轻松管理建议签名者的电子邮件地址。使用可自定义且用户友好的功能，增强您的工作流程。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/signatureline/email/
---
## SignatureLine.Email property

获取或设置建议签名者的电子邮件地址。 此属性的默认值为**空字符串**(Empty ).

```csharp
public string Email { get; set; }
```

## 例子

展示如何创建签名行并将其插入到文档中。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

SignatureLineOptions options = new SignatureLineOptions
{
    AllowComments = true,
    DefaultInstructions = true,
    Email = "john.doe@management.com",
    Instructions = "Please sign here",
    ShowDate = true,
    Signer = "John Doe",
    SignerTitle = "Senior Manager"
};

// 插入一个包含签名线的形状，我们将对其进行外观设计
// 使用我们上面创建的“SignatureLineOptions”对象进行自定义。
// 如果我们插入一个坐标位于页面右下角的形状，
// 我们需要提供负的 x 和 y 坐标来使形状可见。
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0,
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// 通过 Shape 对象验证我们的签名线的属性。
SignatureLine signatureLine = shape.SignatureLine;

Assert.AreEqual("john.doe@management.com", signatureLine.Email);
Assert.AreEqual("John Doe", signatureLine.Signer);
Assert.AreEqual("Senior Manager", signatureLine.SignerTitle);
Assert.AreEqual("Please sign here", signatureLine.Instructions);
Assert.True(signatureLine.ShowDate);
Assert.True(signatureLine.AllowComments);
Assert.True(signatureLine.DefaultInstructions);

doc.Save(ArtifactsDir + "Shape.SignatureLine.docx");
```

### 也可以看看

* class [SignatureLine](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
