---
title: Body.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "Body.parent_section property. Gets the parent section of this story."
type: docs
weight: 30
url: /ar/python-net/aspose.words/body/parent_section/
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
    # أنشئ مستندًا جديدًا
    doc = aw.Document()
    # أنشئ قسمًا وألحقه بالمستند
    section = aw.Section(doc)
    doc.append_child(section)
    # أنشئ جسمًا وألحقه بالقسم
    body = aw.Body(doc)
    section.append_child(body)
    # تحقق من علاقة الأب والابن
    self.assertEqual(section, body.parent_node)
    # أنشئ فقرة وألحقها بالجسم
    para = aw.Paragraph(doc)
    body.append_child(para)
    # تحقق من علاقة الأب والابن
    self.assertEqual(body, para.parent_node)
    # استخدم DocumentBuilder لملء المستند
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
    # بشكل افتراضي، يقوم المستند بتجميع جميع الهوامش الختامية في نهايته.
    self.assertEqual(aw.notes.EndnotePosition.END_OF_DOCUMENT, doc.endnote_options.position)
    # نستخدم خاصية "position" لكائن "EndnoteOptions" الخاص بالمستند
    # لجمع الهوامش الختامية في نهاية كل قسم بدلاً من ذلك.
    doc.endnote_options.position = aw.notes.EndnotePosition.END_OF_SECTION
    insert_section_with_endnote(doc, 'Section 1', 'Endnote 1, will stay in section 1')
    insert_section_with_endnote(doc, 'Section 2', 'Endnote 2, will be pushed down to section 3')
    insert_section_with_endnote(doc, 'Section 3', 'Endnote 3, will stay in section 3')
    # أثناء إظهار الأقسام لهوامشها الختامية، يمكننا ضبط علامة "suppress_endnotes"
    # للكائن "page_setup" الخاص بالقسم إلى "True" للعودة إلى السلوك الافتراضي وتمرير الهوامش الختامية الخاصة به
    # إلى القسم التالي.
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

