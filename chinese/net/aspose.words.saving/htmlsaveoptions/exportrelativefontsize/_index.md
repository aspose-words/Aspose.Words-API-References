---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words for .NET
description: 探索 HtmlSaveOptions ExportRelativeFontSize 属性，自定义 HTML、MHTML 或 EPUB 格式的字体大小。轻松提升可读性！
type: docs
weight: 230
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

指定在保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。 默认值为`错误的`.

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## 评论

在许多现有文档（HTML、IDPF EPUB）中，字体大小都是以相对单位指定的。这允许应用程序在查看/处理文档时调整文本大小。例如，Microsoft Internet Explorer 有“查看-&gt;文本大小”子菜单，Adobe Digital Editions 有两个按钮：增大/减小文本大小。如果您希望此功能正常工作，请设置`ExportRelativeFontSize`财产`真的`.

Aspose Words 文档模型仅包含绝对字体大小单位并仅使用其进行操作。相对单位需要 额外的逻辑，以便根据某个初始（标准）大小重新计算。字体大小**普通的**文档 style 将被作为标准。例如，如果**普通的**有 12pt 字体，有些文本是 18pt，那么它将输出为 output **1.5英寸。**到 HTML。

启用此选项后，除文本外的其他文档元素仍将具有绝对大小。此外，某些与文本相关的属性可能会以绝对大小表示。特别是，使用“精确”规则指定的行距在缩放文本时可能会产生不必要的结果。因此，在使用以下方法导出时，应正确设计和测试源文档：`ExportRelativeFontSize`设置为`真的`。

## 例子

展示如何在保存为 .html 时使用相对字体大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定是否使用相对或绝对字体大小。
// 将“ExportRelativeFontSize”标志设置为“true”以声明字体大小
// 使用“em”测量单位，它是乘以当前字体大小的因子。
// 将“ExportRelativeFontSize”标志设置为“false”以声明字体大小
// 使用“pt”测量单位，即字体的绝对大小（以点为单位）。
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
