---
title: Shape.SignatureLine
second_title: Aspose.Words for .NET API 参考
description: Shape 财产. 获取SignatureLine如果形状是签名线则对象退货 无效的否则
type: docs
weight: 160
url: /zh/net/aspose.words.drawing/shape/signatureline/
---
## Shape.SignatureLine property

获取`SignatureLine`如果形状是签名线，则对象。退货 **无效的**否则。

```csharp
public SignatureLine SignatureLine { get; }
```

### 评论

您可以使用将新的 SignatureLines 插入到文档中[`InsertSignatureLine`](../../../aspose.words/documentbuilder/insertsignatureline/)和

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

* class [SignatureLine](../../signatureline/)
* class [Shape](../)
* 命名空间 [Aspose.Words.Drawing](../../shape/)
* 部件 [Aspose.Words](../../../)


