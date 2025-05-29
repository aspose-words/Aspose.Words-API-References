---
title: Node.ToString
linktitle: ToString
articleTitle: ToString
second_title: Aspose.Words for .NET
description: 探索 Node ToString 方法，轻松将节点内容转换为可自定义格式的字符串，增强数据处理能力。立即优化您的代码！
type: docs
weight: 160
url: /zh/net/aspose.words/node/tostring/
---
## ToString(*[SaveFormat](../../saveformat/)*) {#tostring_1}

将节点的内容导出为指定格式的字符串。

```csharp
public string ToString(SaveFormat saveFormat)
```

### 返回值

指定格式的节点内容。

## 例子

显示在节点上调用 GetText 和 ToString 方法之间的区别。

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertField("MERGEFIELD Field");

// GetText 将检索可见文本以及字段代码和特殊字符。
Assert.AreEqual("\u0013MERGEFIELD Field\u0014«Field»\u0015", doc.GetText().Trim());

// 如果保存为传递的保存格式，ToString 将为我们提供文档的外观。
Assert.AreEqual("«Field»", doc.ToString(SaveFormat.Text).Trim());
```

将节点的内容导出为 HTML 格式的字符串。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// 当我们使用 html SaveFormat 重载调用 ToString 方法时，
// 它将节点的内容转换为其原始 html 表示形式。
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

展示如何提取所有列表项段落的列表标签。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");
doc.UpdateListLabels();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);

// 查找是否有段落列表。在我们的文档中，列表使用纯阿拉伯数字，
// 从三点开始到六点结束。
foreach (Paragraph paragraph in paras.OfType<Paragraph>().Where(p => p.ListFormat.IsListItem).ToList())
{
    Console.WriteLine($"List item paragraph #{paras.IndexOf(paragraph)}");

    // 这是我们将此节点输出为文本格式时得到的文本。
     // 此文本输出将省略列表标签。请修剪所有段落格式字符。
    string paragraphText = paragraph.ToString(SaveFormat.Text).Trim();
    Console.WriteLine($"\tExported Text: {paragraphText}");

    ListLabel label = paragraph.ListLabel;

    // 获取段落在列表当前层级中的位置。如果我们有一个包含多个层的列表，
    // 这将告诉我们它在该级别上的位置。
    Console.WriteLine($"\tNumerical Id: {label.LabelValue}");

    // 将它们组合在一起，将列表标签与文本一起包含在输出中。
    Console.WriteLine($"\tList label combined with text: {label.LabelString} {paragraphText}");
}
```

### 也可以看看

* enum [SaveFormat](../../saveformat/)
* class [Node](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)

---

## ToString(*[SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#tostring_2}

使用指定的保存选项将节点内容导出为字符串。

```csharp
public string ToString(SaveOptions saveOptions)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| saveOptions | SaveOptions | 指定控制如何保存节点的选项。 |

### 返回值

指定格式的节点内容。

## 例子

将节点的内容导出为 HTML 格式的字符串。

```csharp
Document doc = new Document(MyDir + "Document.docx");

Node node = doc.LastSection.Body.LastParagraph;

// 当我们使用 html SaveFormat 重载调用 ToString 方法时，
// 它将节点的内容转换为其原始 html 表示形式。
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
