---
title: ParagraphAlignment enumeration
linktitle: ParagraphAlignment enumeration
articleTitle: ParagraphAlignment enumeration
second_title: Aspose.Words for Python
description: "aspose.words.ParagraphAlignment enumeration. Specifies text alignment in a paragraph."
type: docs
weight: 970
url: /zh/python-net/aspose.words/paragraphalignment/
---

## ParagraphAlignment enumeration

Specifies text alignment in a paragraph.


### Members

| Name | Description |
| --- | --- |
| LEFT | Text is aligned to the left. |
| CENTER | Text is centered horizontally. |
| RIGHT | Text is aligned to the right. |
| JUSTIFY | Text is aligned to both left and right. |
| DISTRIBUTED | Text is evenly distributed. |
| ARABIC_MEDIUM_KASHIDA | Arabic only. Kashida length for text is extended to a medium length determined by the consumer. |
| ARABIC_HIGH_KASHIDA | Arabic only. Kashida length for text is extended to its widest possible length. |
| ARABIC_LOW_KASHIDA | Arabic only. Kashida length for text is extended to a slightly longer length. |
| THAI_DISTRIBUTED | Thai only. Text is justified with an optimization for Thai. |
| MATH_ELEMENT_CENTER_AS_GROUP | The only Math element in a line, aligned as 'Centered As Group'. |

### Examples

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()
# 空白文档包含一个节、一个正文和一个段落。
# 调用 "RemoveAllChildren" 方法以移除所有这些节点，
# 并得到一个没有子节点的文档节点。
doc.remove_all_children()
# 此文档现在没有可添加内容的复合子节点。
# 如果我们想编辑它，需要重新填充其节点集合。
# 首先，创建一个新节，然后将其作为子节点追加到根文档节点。
section = aw.Section(doc)
doc.append_child(section)
# 为该节设置一些页面布局属性。
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER
# 节需要一个正文，用于包含并显示其所有内容
# 在页面上位于节的页眉和页脚之间。
body = aw.Body(doc)
section.append_child(body)
# 创建一个段落，设置一些格式属性，然后将其作为子节点追加到正文。
para = aw.Paragraph(doc)
para.paragraph_format.style_name = 'Heading 1'
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER
body.append_child(para)
# 最后，添加一些内容以完成文档。创建一个 run，
# 设置其外观和内容，然后将其作为子节点追加到段落。
run = aw.Run(doc=doc)
run.text = 'Hello World!'
run.font.color = aspose.pydrawing.Color.red
para.append_child(run)
self.assertEqual('Hello World!', doc.get_text().strip())
doc.save(file_name=ARTIFACTS_DIR + 'Section.CreateManually.docx')
```

### See Also

* module [aspose.words](../)

