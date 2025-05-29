---
title: StructuredDocumentTag.IsTemporary
linktitle: IsTemporary
articleTitle: IsTemporary
second_title: Aspose.Words for .NET
description: 了解 StructuredDocumentTag IsTemporary 属性如何确定内容更改后 SDT 是否从 WordProcessingML 中移除。立即优化您的文档！
type: docs
weight: 160
url: /zh/net/aspose.words.markup/structureddocumenttag/istemporary/
---
## StructuredDocumentTag.IsTemporary property

指定此**特殊和差别待遇**当其内容被修改时，应从 WordProcessingML 文档中删除。

```csharp
public bool IsTemporary { get; set; }
```

## 例子

展示如何制作一次性控件。

```csharp
Document doc = new Document();

// 插入纯文本结构化文档标签，
// 它将充当用户可以输入文本的纯文本表单。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 将“IsTemporary”属性设置为“true”，以使结构化文档标签消失，并且
// 用户在 Microsoft Word 中编辑一次后，将其内容吸收到文档中。
// 将“IsTemporary”属性设置为“false”以允许用户编辑内容
// 结构化文档标签任意次数。
tag.IsTemporary = isTemporary;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Please enter text: ");
builder.InsertNode(tag);

// 以复选框的形式插入另一个结构化文档标签，并将其默认状态设置为“已选中”。
tag = new StructuredDocumentTag(doc, SdtType.Checkbox, MarkupLevel.Inline);
tag.Checked = true;

// 将“IsTemporary”属性设置为“true”，使复选框变成一个符号
// 一旦用户在 Microsoft Word 中单击它。
// 将“IsTemporary”属性设置为“false”以允许用户任意次数单击复选框。
tag.IsTemporary = isTemporary;

builder.Write("\nPlease click the check box: ");
builder.InsertNode(tag);

doc.Save(ArtifactsDir + "StructuredDocumentTag.IsTemporary.docx");
```

### 也可以看看

* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../../aspose.words.markup/)
* 部件 [Aspose.Words](../../../)
