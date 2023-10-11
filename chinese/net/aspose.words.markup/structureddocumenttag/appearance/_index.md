---
title: StructuredDocumentTag.Appearance
second_title: Aspose.Words for .NET API 参考
description: StructuredDocumentTag 财产. 获取/设置结构化文档标签的外观
type: docs
weight: 20
url: /zh/net/aspose.words.markup/structureddocumenttag/appearance/
---
## StructuredDocumentTag.Appearance property

获取/设置结构化文档标签的外观。

```csharp
public SdtAppearance Appearance { get; set; }
```

### 例子

演示如何在纯文本框中创建结构化文档标签并修改其外观。

```csharp
Document doc = new Document();

// 创建一个包含纯文本的结构化文档标签。
StructuredDocumentTag tag = new StructuredDocumentTag(doc, SdtType.PlainText, MarkupLevel.Inline);

// 设置当鼠标悬停在 Microsoft Word 中的结构化文档标签上时出现的框架的标题和颜色。
tag.Title = "My plain text";
tag.Color = Color.Magenta;

// 为这个结构化文档标签设置一个标签，可以获取
// 作为名为“tag”的 XML 元素，其“@val”属性中包含以下字符串。
tag.Tag = "MyPlainTextSDT";

// 每个结构化文档标签都有一个随机的唯一 ID。
Assert.That(tag.Id, Is.Positive);

// 设置结构化文档标签内文本的字体。
tag.ContentsFont.Name = "Arial";

// 设置结构化文档标签末尾文本的字体。
// 使用箭头键移出标签后在文档正文中键入的任何文本都将使用此字体。
tag.EndCharacterFont.Name = "Arial Black";

// 默认情况下，这是 false，并且在结构化文档标签内按 Enter 键不会执行任何操作。
// 当设置为 true 时，我们的结构化文档标签可以有多行。

// 将“Multiline”属性设置为“false”以仅允许内容
// 此结构化文档标记跨越一行。
// 将“Multiline”属性设置为“true”以允许标签包含多行内容。
tag.Multiline = true;

// 将“Appearance”属性设置为“SdtAppearance.Tags”以在内容周围显示标签。
 // 默认情况下，结构化文档标签显示为 BoundingBox。
tag.Appearance = SdtAppearance.Tags;

DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertNode(tag);

// 在新段落中插入结构化文档标签的克隆。
StructuredDocumentTag tagClone = (StructuredDocumentTag)tag.Clone(true);
builder.InsertParagraph();
builder.InsertNode(tagClone);

// 使用“RemoveSelfOnly”方法删除结构化文档标签，同时保留其内容在文档中。
tagClone.RemoveSelfOnly();

doc.Save(ArtifactsDir + "StructuredDocumentTag.PlainText.docx");
```

### 也可以看看

* enum [SdtAppearance](../../sdtappearance/)
* class [StructuredDocumentTag](../)
* 命名空间 [Aspose.Words.Markup](../../structureddocumenttag/)
* 部件 [Aspose.Words](../../../)


