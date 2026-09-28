---
title: PageSetup.suppress_endnotes property
linktitle: suppress_endnotes property
articleTitle: suppress_endnotes property
second_title: Aspose.Words for Python
description: "PageSetup.suppress_endnotes property. True if endnotes are printed at the end of the next section that doesn't suppress endnotes"
type: docs
weight: 410
url: /zh/python-net/aspose.words/pagesetup/suppress_endnotes/
---

## PageSetup.suppress_endnotes property

True if endnotes are printed at the end of the next section that doesn't suppress endnotes.
Suppressed endnotes are printed before the endnotes in that section.


```python
@property
def suppress_endnotes(self) -> bool:
    ...

@suppress_endnotes.setter
def suppress_endnotes(self, value: bool):
    ...

```

### Examples

Shows how to store endnotes at the end of each section, and modify their positions (InsertSectionWithEndnote).

```python
@staticmethod
def _insert_section_with_endnote(doc, section_body_text, endnote_text):
    import aspose.words as aw
    from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
    # 创建一个新文档
    doc = aw.Document()
    # 创建一个节并将其追加到文档中
    section = aw.Section(doc)
    doc.append_child(section)
    # 创建一个正文并将其追加到节中
    body = aw.Body(doc)
    section.append_child(body)
    # 验证父子关系
    self.assertEqual(section, body.parent_node)
    # 创建一个段落并将其追加到正文中
    para = aw.Paragraph(doc)
    body.append_child(para)
    # 验证父子关系
    self.assertEqual(body, para.parent_node)
    # 使用 DocumentBuilder 填充文档
    builder = aw.DocumentBuilder(doc=doc)
    builder.move_to(para)
    builder.write(section_body_text)
    builder.insert_footnote(footnote_type=aw.notes.FootnoteType.ENDNOTE, footnote_text=endnote_text)
```

Shows how to store endnotes at the end of each section, and modify their positions.

```python
def suppress_endnotes():
    doc = aw.Document()
    doc.remove_all_children()
    # 默认情况下，文档会将所有尾注编译在文档末尾。
    self.assertEqual(aw.notes.EndnotePosition.END_OF_DOCUMENT, doc.endnote_options.position)
    # 我们使用文档的 "EndnoteOptions" 对象的 "position" 属性
    # 以便将尾注收集在每个章节的末尾。
    doc.endnote_options.position = aw.notes.EndnotePosition.END_OF_SECTION
    insert_section_with_endnote(doc, 'Section 1', 'Endnote 1, will stay in section 1')
    insert_section_with_endnote(doc, 'Section 2', 'Endnote 2, will be pushed down to section 3')
    insert_section_with_endnote(doc, 'Section 3', 'Endnote 3, will stay in section 3')
    # 在获取章节以显示各自的尾注时，我们可以设置 "suppress_endnotes" 标志
    # 将章节的 "page_setup" 对象的该标志设为 "True"，以恢复默认行为并传递其尾注
    # 到下一个章节。
    page_setup = doc.sections[1].page_setup
    page_setup.suppress_endnotes = True
    doc.save(ARTIFACTS_DIR + 'PageSetup.suppress_endnotes.docx')

def insert_section_with_endnote(doc: aw.Document, section_body_text: str, endnote_text: str):
    """Append a section with text and an endnote to a document."""
    section = aw.Section(doc)
    doc.append_child(section)
    body = aw.Body(doc)
    section.append_child(body)
    self.assertEqual(section, body.parent_node)
    para = aw.Paragraph(doc)
    body.append_child(para)
    self.assertEqual(body, para.parent_node)
    builder = aw.DocumentBuilder(doc)
    builder.move_to(para)
    builder.write(section_body_text)
    builder.insert_footnote(aw.notes.FootnoteType.ENDNOTE, endnote_text)
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

