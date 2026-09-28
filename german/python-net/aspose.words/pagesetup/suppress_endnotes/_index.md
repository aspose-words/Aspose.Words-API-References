---
title: PageSetup.suppress_endnotes property
linktitle: suppress_endnotes property
articleTitle: suppress_endnotes property
second_title: Aspose.Words for Python
description: "PageSetup.suppress_endnotes property. True if endnotes are printed at the end of the next section that doesn't suppress endnotes"
type: docs
weight: 410
url: /de/python-net/aspose.words/pagesetup/suppress_endnotes/
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
    # Erstellen Sie ein neues Dokument
    doc = aw.Document()
    # Erstellen Sie einen Abschnitt und fügen Sie ihn dem Dokument hinzu
    section = aw.Section(doc)
    doc.append_child(section)
    # Erstellen Sie einen Body und fügen Sie ihn dem Abschnitt hinzu
    body = aw.Body(doc)
    section.append_child(body)
    # Überprüfen Sie die Eltern‑Kind-Beziehung
    self.assertEqual(section, body.parent_node)
    # Erstellen Sie einen Absatz und fügen Sie ihn dem Body hinzu
    para = aw.Paragraph(doc)
    body.append_child(para)
    # Überprüfen Sie die Eltern‑Kind-Beziehung
    self.assertEqual(body, para.parent_node)
    # Verwenden Sie DocumentBuilder, um das Dokument zu füllen
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
    # Standardmäßig sammelt ein Dokument alle Endnoten am Ende.
    self.assertEqual(aw.notes.EndnotePosition.END_OF_DOCUMENT, doc.endnote_options.position)
    # Wir verwenden die Eigenschaft "position" des "EndnoteOptions"-Objekts des Dokuments
    # um stattdessen Endnoten am Ende jedes Abschnitts zu sammeln.
    doc.endnote_options.position = aw.notes.EndnotePosition.END_OF_SECTION
    insert_section_with_endnote(doc, 'Section 1', 'Endnote 1, will stay in section 1')
    insert_section_with_endnote(doc, 'Section 2', 'Endnote 2, will be pushed down to section 3')
    insert_section_with_endnote(doc, 'Section 3', 'Endnote 3, will stay in section 3')
    # Während wir Abschnitte dazu bringen, ihre jeweiligen Endnoten anzuzeigen, können wir das Flag "suppress_endnotes" setzen
    # des "page_setup"-Objekts eines Abschnitts auf "True", um zum Standardverhalten zurückzukehren und seine Endnoten weiterzugeben
    # auf den nächsten Abschnitt.
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

