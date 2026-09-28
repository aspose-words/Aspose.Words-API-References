---
title: Body.parent_section property
linktitle: parent_section property
articleTitle: parent_section property
second_title: Aspose.Words for Python
description: "Body.parent_section property. Gets the parent section of this story."
type: docs
weight: 30
url: /fr/python-net/aspose.words/body/parent_section/
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
    # Créez un nouveau document
    doc = aw.Document()
    # Créez une section et ajoutez‑la au document
    section = aw.Section(doc)
    doc.append_child(section)
    # Créez un corps et ajoutez‑le à la section
    body = aw.Body(doc)
    section.append_child(body)
    # Vérifiez la relation parent‑enfant
    self.assertEqual(section, body.parent_node)
    # Créez un paragraphe et ajoutez‑le au corps
    para = aw.Paragraph(doc)
    body.append_child(para)
    # Vérifiez la relation parent‑enfant
    self.assertEqual(body, para.parent_node)
    # Utilisez DocumentBuilder pour remplir le document
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
    # Par défaut, un document compile toutes les notes de fin à la fin.
    self.assertEqual(aw.notes.EndnotePosition.END_OF_DOCUMENT, doc.endnote_options.position)
    # Nous utilisons la propriété "position" de l'objet "EndnoteOptions" du document
    # pour collecter les notes de fin à la fin de chaque section à la place.
    doc.endnote_options.position = aw.notes.EndnotePosition.END_OF_SECTION
    insert_section_with_endnote(doc, 'Section 1', 'Endnote 1, will stay in section 1')
    insert_section_with_endnote(doc, 'Section 2', 'Endnote 2, will be pushed down to section 3')
    insert_section_with_endnote(doc, 'Section 3', 'Endnote 3, will stay in section 3')
    # Lors de l'affichage des notes de fin par les sections, nous pouvons définir le drapeau "suppress_endnotes"
    # de l'objet "page_setup" d'une section à "True" pour revenir au comportement par défaut et transmettre ses notes de fin
    # à la section suivante.
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

