---
title: ImportFormatOptions.IgnoreTextBoxes
linktitle: IgnoreTextBoxes
articleTitle: IgnoreTextBoxes
second_title: 用于 .NET 的 Aspose.Words
description: ImportFormatOptions IgnoreTextBoxes 财产. 获取或设置一个布尔值该值指定忽略文本框内容的源格式 ifKeepSourceFormatting使用模式 默认值为真的 在 C#.
type: docs
weight: 50
url: /zh/net/aspose.words/importformatoptions/ignoretextboxes/
---
## ImportFormatOptions.IgnoreTextBoxes property

获取或设置一个布尔值，该值指定忽略文本框内容的源格式 ifKeepSourceFormatting使用模式。 默认值为`真的`.

```csharp
public bool IgnoreTextBoxes { get; set; }
```

## 例子

演示如何在附加文档时管理文本框格式。

```csharp
// 创建一个文档，将另一个文档中的节点插入其中。
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

builder.Writeln("Hello world!");

// 创建另一个带有文本框的文档，我们将其导入到第一个文档中。
Document srcDoc = new Document();
builder = new DocumentBuilder(srcDoc);

Shape textBox = builder.InsertShape(ShapeType.TextBox, 300, 100);
builder.MoveTo(textBox.FirstParagraph);
builder.ParagraphFormat.Style.Font.Name = "Courier New";
builder.ParagraphFormat.Style.Font.Size = 24;
builder.Write("Textbox contents");

// 设置一个标志来指定是清除还是保留文本框格式
// 将它们导入其他文档时。
ImportFormatOptions importFormatOptions = new ImportFormatOptions();
importFormatOptions.IgnoreTextBoxes = ignoreTextBoxes;

// 将源文档中的文本框导入到目标文档中，
// 然后验证我们是否保留了其文本内容的样式。
NodeImporter importer = new NodeImporter(srcDoc, dstDoc, ImportFormatMode.KeepSourceFormatting, importFormatOptions);
Shape importedTextBox = (Shape)importer.ImportNode(textBox, true);
dstDoc.FirstSection.Body.Paragraphs[1].AppendChild(importedTextBox);

if (ignoreTextBoxes)
{
    Assert.AreEqual(12.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Times New Roman", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}
else
{
    Assert.AreEqual(24.0d, importedTextBox.FirstParagraph.Runs[0].Font.Size);
    Assert.AreEqual("Courier New", importedTextBox.FirstParagraph.Runs[0].Font.Name);
}

dstDoc.Save(ArtifactsDir + "DocumentBuilder.IgnoreTextBoxes.docx");
```

### 也可以看看

* class [ImportFormatOptions](../)
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
