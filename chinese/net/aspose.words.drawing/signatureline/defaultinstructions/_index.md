---
title: SignatureLine.DefaultInstructions
linktitle: DefaultInstructions
articleTitle: DefaultInstructions
second_title: 用于 .NET 的 Aspose.Words
description: SignatureLine DefaultInstructions 财产. 获取或设置一个值该值指示默认说明显示在签名对话框中 此属性的默认值为真的 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/signatureline/defaultinstructions/
---
## SignatureLine.DefaultInstructions property

获取或设置一个值，该值指示默认说明显示在“签名”对话框中。 此属性的默认值为`真的`.

```csharp
public bool DefaultInstructions { get; set; }
```

## 例子

演示如何创建签名行并将其插入文档中。

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

// 插入一个包含签名线的形状，我们将其外观
// 使用我们上面创建的“SignatureLineOptions”对象进行自定义。
// 如果我们插入一个坐标源自页面右下角的形状，
// 我们需要提供负的 x 和 y 坐标才能将形状带入视图。
Shape shape = builder.InsertSignatureLine(options, RelativeHorizontalPosition.RightMargin, -170.0, 
        RelativeVerticalPosition.BottomMargin, -60.0, WrapType.None);

Assert.True(shape.IsSignatureLine);

// 通过 Shape 对象验证签名线的属性。
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
