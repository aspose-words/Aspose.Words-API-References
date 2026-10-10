---
title: Body.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "Body.parent_section property. Gets the parent section of this story."
type: docs
weight: 30
url: /ru/python-net/aspose.words/body/parent_section/
---

## Body.parent_section property

Gets the parent section of this story.


```python
@property
def parent_section(self) -> aspose.words.Section:
    ...

```

### Remarks

[Body.parent_section](./) is equivalent to [Node.parent_node](../../node/parent_node/) casted to [Section](../../section/).




### Examples

Shows how to store endnotes at the end of each section, and modify their positions (InsertSectionWithEndnote).

```python
@staticmethod
def _insert_section_with_endnote(doc, section_body_text, endnote_text):
    import aspose.words as aw
    from api_example_base import ApiExampleBase, MY_DIR, ARTIFACTS_DIR, GOLDS_DIR, TEMP_DIR, IMAGE_DIR, FONTS_DIR
    # Создайте новый документ
    doc = aw.Document()
    # Создайте раздел и добавьте его в документ
    section = aw.Section(doc)
    doc.append_child(section)
    # Создайте тело и добавьте его в раздел
    body = aw.Body(doc)
    section.append_child(body)
    # Проверьте отношение родитель‑дитя
    self.assertEqual(section, body.parent_node)
    # Создайте абзац и добавьте его в тело
    para = aw.Paragraph(doc)
    body.append_child(para)
    # Проверьте отношение родитель‑дитя
    self.assertEqual(body, para.parent_node)
    # Используйте DocumentBuilder для заполнения документа
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
    # По умолчанию документ собирает все концевые сноски в конце.
    self.assertEqual(aw.notes.EndnotePosition.END_OF_DOCUMENT, doc.endnote_options.position)
    # Мы используем свойство "position" объекта "EndnoteOptions" документа
    # чтобы собирать концевые сноски в конце каждого раздела вместо этого.
    doc.endnote_options.position = aw.notes.EndnotePosition.END_OF_SECTION
    insert_section_with_endnote(doc, 'Section 1', 'Endnote 1, will stay in section 1')
    insert_section_with_endnote(doc, 'Section 2', 'Endnote 2, will be pushed down to section 3')
    insert_section_with_endnote(doc, 'Section 3', 'Endnote 3, will stay in section 3')
    # При получении разделов для отображения их соответствующих концевых сносок мы можем установить флаг "suppress_endnotes"
    # объекта "page_setup" раздела в "True", чтобы вернуть поведение по умолчанию и передать его концевые сноски
    # в следующий раздел.
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
* class [Body](../)

