---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions ExportRelativeFontSize 财产. 指定在保存为 HTMLMHTML 或 EPUB 时是否应以相对单位输出字体大小 默认为错误的 在 C#.
type: docs
weight: 230
url: /zh/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

指定在保存为 HTML、MHTML 或 EPUB 时是否应以相对单位输出字体大小。 默认为`错误的`.

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## 评论

在许多现有文档（HTML、IDPF EPUB）中，字体大小以相对单位指定。这允许 应用程序在查看/处理文档时调整文本大小。例如，Microsoft Internet Explorer 有“查看-&gt;文本大小”子菜单，Adobe Digital Editions 有两个按钮：增加/减小文本大小。 如果您希望此功能起作用，请设置`ExportRelativeFontSize`财产`真的`.

Aspose Words 文档模型包含并且仅使用绝对字体大小单位进行操作。相对单位需要 附加逻辑才能从某个初始（标准）大小重新计算。字体大小**普通的**文档样式 被视为标准。例如，如果**普通的**有 12pt 字体，有些文本是 18pt，那么它将输出 为**1.5em。**到 HTML。

启用此选项后，文本以外的文档元素仍将具有绝对大小。还有一些 文本相关的属性可能是绝对表达的。特别是，使用“精确”规则 指定的行距可能会在缩放文本时产生不需要的结果。因此，在导出时应正确设计和测试源文档 `ExportRelativeFontSize`调成`真的`.

## 例子

显示保存为 .html 时如何使用相对字体大小。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定是使用相对还是绝对字体大小。
// 将“ExportRelativeFontSize”标志设置为“true”以声明字体大小
// 使用“em”测量单位，它是乘以当前字体大小的因子。
// 将“ExportRelativeFontSize”标志设置为“false”以声明字体大小
// 使用“pt”测量单位，即字体的绝对大小（以磅为单位）。
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
