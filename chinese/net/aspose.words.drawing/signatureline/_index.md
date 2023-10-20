---
title: SignatureLine Class
linktitle: SignatureLine
articleTitle: SignatureLine
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.SignatureLine 班级. 提供对签名行属性的访问 在 C#.
type: docs
weight: 1300
url: /zh/net/aspose.words.drawing/signatureline/
---
## SignatureLine class

提供对签名行属性的访问。

要了解更多信息，请访问[使用数字签名](https://docs.aspose.com/words/net/working-with-digital-signatures/)文档文章。

```csharp
public class SignatureLine
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [AllowComments](../../aspose.words.drawing/signatureline/allowcomments/) { get; set; } | 获取或设置一个值，该值指示签名者可以在“签名”对话框中添加注释。 此属性的默认值为`错误的`. |
| [DefaultInstructions](../../aspose.words.drawing/signatureline/defaultinstructions/) { get; set; } | 获取或设置一个值，该值指示默认说明显示在“签名”对话框中。 此属性的默认值为`真的`. |
| [Email](../../aspose.words.drawing/signatureline/email/) { get; set; } | 获取或设置建议签名者的电子邮件地址。 此属性的默认值为**空字符串**（Empty). |
| [Id](../../aspose.words.drawing/signatureline/id/) { get; set; } | 获取或设置此签名行的标识符。 |
| [Instructions](../../aspose.words.drawing/signatureline/instructions/) { get; set; } | 获取或设置在签署签名行时显示的给签名者的说明。 如果满足以下条件，则忽略此属性：[`DefaultInstructions`](./defaultinstructions/)已设置。 此属性的默认值为**空字符串**（Empty). |
| [IsSigned](../../aspose.words.drawing/signatureline/issigned/) { get; } | 表示签名行由数字签名签名。 |
| [IsValid](../../aspose.words.drawing/signatureline/isvalid/) { get; } | 表示签名行是由数字签名签署的，并且该数字签名有效。 |
| [ProviderId](../../aspose.words.drawing/signatureline/providerid/) { get; set; } | 获取或设置此签名行的签名提供程序标识符。 默认值为“{00000000-0000-0000-0000-000000000000}”。 |
| [ShowDate](../../aspose.words.drawing/signatureline/showdate/) { get; set; } | 获取或设置一个值，该值指示签名日期显示在签名行中。 此属性的默认值为`真的`. |
| [Signer](../../aspose.words.drawing/signatureline/signer/) { get; set; } | 获取或设置签名行的建议签名者。 此属性的默认值为**空字符串**（Empty). |
| [SignerTitle](../../aspose.words.drawing/signatureline/signertitle/) { get; set; } | 获取或设置建议签名者的头衔（例如，经理）。 此属性的默认值为**空字符串**（Empty). |

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

* 命名空间 [Aspose.Words.Drawing](../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../)
