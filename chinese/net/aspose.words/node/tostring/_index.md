---
title: Node.ToString
second_title: Aspose.Words for .NET API 参考
description: Node 方法. 将节点的内容导出为指定格式的字符串
type: docs
weight: 160
url: /zh/net/aspose.words/node/tostring/
---
## ToString(SaveFormat) {#tostring_1}

将节点的内容导出为指定格式的字符串。

```csharp
public string ToString(SaveFormat saveFormat)
```

### 返回值

指定格式的节点内容。

### 例子

显示在节点上调用 GetText 和 ToString 方法之间的区别。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText 将检索可见文本以及域代码和特殊字符。
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015\u000c", doc.GetText());

// 如果保存为传递的保存格式，ToString 将为我们提供文档的外观。
Assert.AreEqual("«Field»\r\n", doc.ToString(SaveFormat.Text));
```

将节点的内容导出为 HTML 格式的字符串。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// 当我们使用 html SaveFormat 重载调用 ToString 方法时，
// 它将节点的内容转换为它们的原始 html 表示。
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// 我们还可以使用 SaveOptions 对象修改此转换的结果。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

演示如何提取作为列表项的所有段落的列表标签。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// 查找我们是否有段落列表。在我们的文档中，我们的列表使用纯阿拉伯数字，
// 从三点开始，六点结束。
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem))
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // 这是我们将此节点输出为文本格式时得到的文本。
    // 此文本输出将省略列表标签。修剪任何段落格式字符。 
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // 这将获取段落在列表当前级别中的位置。如果我们有一个包含多个级别的列表，
    // 这将告诉我们它在那个级别上的位置。
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // 将它们组合在一起以在输出中包含列表标签和文本。
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### 也可以看看

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../node/)
* 部件 [Aspose.Words](../../../)

---

## ToString(SaveOptions) {#tostring_2}

使用指定的保存选项将节点的内容导出为字符串。

```csharp
public string ToString(SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | SaveOptions | 指定控制节点保存方式的选项。 |

### 返回值

指定格式的节点内容。

### 例子

将节点的内容导出为 HTML 格式的字符串。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// 当我们使用 html SaveFormat 重载调用 ToString 方法时，
// 它将节点的内容转换为它们的原始 html 表示。
Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%; font-size:12pt\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(SaveFormat.Html));

// 我们还可以使用 SaveOptions 对象修改此转换的结果。
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.ExportRelativeFontSize = true;

Assert.AreEqual("<p style=\"margin-top:0pt; margin-bottom:8pt; line-height:108%\">" +
                "<span style=\"font-family:'Times New Roman'\">Hello World!</span>" +
                "</p>", node.ToString(saveOptions));
```

### 也可以看看

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../node/)
* 部件 [Aspose.Words](../../../)


