---
title: SignatureLine.Email
second_title: Aspose.Words for .NET API 参考
description: SignatureLine 财产. 获取或设置建议的签名者的电子邮件地址 此属性的默认值为 空字符串Empty .
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/signatureline/email/
---
## SignatureLine.Email property

获取或设置建议的签名者的电子邮件地址。 此属性的默认值为 **空字符串**(Empty ).

```csharp
public string Email { get; set; }
```

### 例子

演示如何为签名创建一行并将其插入到文档中。

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

// 插入一个包含签名线的形状，我们将看到它的外观
// 使用我们在上面创建的“SignatureLineOptions”对象进行自定义。
// 如果我们插入一个坐标起源于页面右下角的形状，
// 我们需要提供负的 x 和 y 坐标才能将形状显示在视图中。
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// 通过其 Shape 对象验证我们的签名线的属性。
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
* 命名空间 [Aspose.Words.Drawing](../../signatureline/)
* 部件 [Aspose.Words](../../../)


