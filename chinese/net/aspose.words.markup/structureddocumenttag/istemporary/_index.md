---
title: StructuredDocumentTag.IsTemporary
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 财产. 指定是否 特殊测试当其内容 被修改时应从WordProcessingML文档中删除
type: docs
weight: 160
url: /zh/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

指定是否 **特殊测试**当其内容 被修改时，应从WordProcessingML文档中删除。

```csharp
public bool IsTemporary { get; set; }
```

### 例子

展示如何制作一次性控件。

```csharp
Document doc = new Document();

// 插入纯文本结构化文档标签，
// 它将充当用户可以输入文本的纯文本表单。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“IsTemporary”属性设置为“true”，使结构化文档标签消失并
// 用户在 Microsoft Word 中编辑一次后，将其内容吸收到文档中。
// 将“IsTemporary”属性设置为“false”以允许用户编辑内容
// 结构化文档标签任意次。
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// 以复选框的形式插入另一个结构化文档标签，并将其默认状态设置为“已选中”。
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// 将“IsTemporary”属性设置为“true”，使复选框成为一个符号
// 一旦用户在 Microsoft Word 中单击它。
// 将“IsTemporary”属性设置为“false”以允许用户多次单击该复选框。
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


