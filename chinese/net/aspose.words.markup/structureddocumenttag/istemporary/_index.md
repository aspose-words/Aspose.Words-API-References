---
title: StructuredDocumentTag.IsTemporary
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 财产. 指定这是否 SDT当其 contents 被修改时应从 WordProcessingML 文档中删除
type: docs
weight: 160
url: /zh/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

指定这是否 **SDT**当其 contents 被修改时，应从 WordProcessingML 文档中删除。

```csharp
public bool IsTemporary { get; set; }
```

### 例子

展示如何制作一次性控件。

```csharp
Document doc = new Document();

// 插入纯文本结构化文档标签，
// 这将充当用户可以输入文本的纯文本表单。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“IsTemporary”属性设置为“true”，使结构化文档标签消失，
// 用户在 Microsoft Word 中编辑一次后，将其内容同化到文档中。
// 将“IsTemporary”属性设置为“false”以允许用户编辑内容
// 结构化文档标签的任意次数。
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// 以复选框的形式插入另一个结构化文档标签，并将其默认状态设置为“选中”。
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// 将“IsTemporary”属性设置为“true”，使复选框成为符号
// 一旦用户在 Microsoft Word 中单击它。
// 将“IsTemporary”属性设置为“false”，以允许用户多次单击复选框。
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


