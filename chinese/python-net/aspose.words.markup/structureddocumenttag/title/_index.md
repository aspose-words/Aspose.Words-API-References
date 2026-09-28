---
title: StructuredDocumentTag.title property
linktitle: title property
articleTitle: title property
second_title: Aspose.Words for Python
description: "StructuredDocumentTag.title property. Specifies the friendly name associated with this SDT"
type: docs
weight: 290
url: /zh/python-net/aspose.words.markup/structureddocumenttag/title/
---

## StructuredDocumentTag.title property

Specifies the friendly name associated with this **SDT**.
Can not be ``None``.



```python
@property
def title(self) -> str:
    ...

@title.setter
def title(self, value: str):
    ...

```

### Examples

Shows how to create a structured document tag in a plain text box and modify its appearance.

```python
doc = aw.Document()
# 创建一个将包含纯文本的结构化文档标签。
tag = aw.markup.StructuredDocumentTag(doc, aw.markup.SdtType.PLAIN_TEXT, aw.markup.MarkupLevel.INLINE)
# 设置在 Microsoft Word 中将鼠标悬停在结构化文档标签上时出现的框架的标题和颜色。
tag.title = 'My plain text'
tag.color = aspose.pydrawing.Color.magenta
# 为此结构化文档标签设置一个可获取的标签
# 作为名为 "tag" 的 XML 元素，在其 "@val" 属性中放置以下字符串。
tag.tag = 'MyPlainTextSDT'
# 每个结构化文档标签都有一个随机唯一的 ID。
self.assertTrue(tag.id > 0)
# 设置结构化文档标签内部文本的字体。
tag.contents_font.name = 'Arial'
# 设置结构化文档标签末尾文本的字体。
# 在使用方向键移出标签后，在文档正文中键入的任何文本都将使用此字体。
tag.end_character_font.name = 'Arial Black'
# 默认情况下，此值为 false，在结构化文档标签内部按回车键不会有任何作用。
# 当设置为 true 时，我们的结构化文档标签可以包含多行。
# 将 "Multiline" 属性设为 "false"，仅允许内容
# 此结构化文档标签的内容跨越单行。
# 将 "Multiline" 属性设为 "true"，以允许标签包含多行内容。
tag.multiline = True
# 将 "Appearance" 属性设为 "SdtAppearance.Tags"，以在内容周围显示标签。
# 默认情况下，结构化文档标签显示为 BoundingBox。
tag.appearance = aw.markup.SdtAppearance.TAGS
builder = aw.DocumentBuilder(doc=doc)
builder.insert_node(tag)
# 在新段落中插入我们结构化文档标签的克隆。
tag_clone = tag.clone(True).as_structured_document_tag()
builder.insert_paragraph()
builder.insert_node(tag_clone)
# 使用 "RemoveSelfOnly" 方法删除结构化文档标签，同时保留其内容在文档中。
tag_clone.remove_self_only()
doc.save(file_name=ARTIFACTS_DIR + 'StructuredDocumentTag.PlainText.docx')
```

### See Also

* module [aspose.words.markup](../../)
* class [StructuredDocumentTag](../)

