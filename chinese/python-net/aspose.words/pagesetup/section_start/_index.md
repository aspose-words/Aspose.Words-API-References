---
title: PageSetup.section_start property
linktitle: section_start property
articleTitle: section_start property
second_title: Aspose.Words for Python
description: "PageSetup.section_start property. Returns or sets the type of section break for the specified object."
type: docs
weight: 390
url: /zh/python-net/aspose.words/pagesetup/section_start/
---

## PageSetup.section_start property

Returns or sets the type of section break for the specified object.


```python
@property
def section_start(self) -> aspose.words.SectionStart:
    ...

@section_start.setter
def section_start(self, value: aspose.words.SectionStart):
    ...

```

### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('This text is in section 1.')
# 分节符类型决定新节如何与前一节分离。
# 以下是五种分节符类型。
# 1 -  在新页面上开始下一节：
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('This text is in section 2.')
self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)
# 2 -  在当前页面上开始下一节：
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln('This text is in section 3.')
self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)
# 3 -  在新偶数页上开始下一节：
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln('This text is in section 4.')
self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)
# 4 -  在新奇数页上开始下一节：
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln('This text is in section 5.')
self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)
# 5 -  在新列上开始下一节：
columns = builder.page_setup.text_columns
columns.set_count(2)
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln('This text is in section 6.')
self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.SetSectionStart.docx')
```

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

* module [aspose.words](../../)
* class [PageSetup](../)

