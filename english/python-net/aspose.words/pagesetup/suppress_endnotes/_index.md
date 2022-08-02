---
title: suppress_endnotes property
second_title: Aspose.Words for Python via .NET API Reference
description: "True if endnotes are printed at the end of the next section that doesn't suppress endnotes"
type: docs
weight: 400
url: /python-net/aspose.words/pagesetup/suppress_endnotes/
---

## PageSetup.suppress_endnotes property

**True** if endnotes are printed at the end of the next section that doesn't suppress endnotes.
Suppressed endnotes are printed before the endnotes in that section.



### Examples

Shows how to store endnotes at the end of each section, and modify their positions.

```python
def test_suppress_endnotes(self):

    doc = aw.Document()
    doc.remove_all_children()

    # By default, a document compiles all endnotes at its end.
    self.assertEqual(aw.notes.EndnotePosition.END_OF_DOCUMENT, doc.endnote_options.position)

    # We use the "position" property of the document's "EndnoteOptions" object
    # to collect endnotes at the end of each section instead.
    doc.endnote_options.position = aw.notes.EndnotePosition.END_OF_SECTION

    self.insert_section_with_endnote(doc, "Section 1", "Endnote 1, will stay in section 1")
    self.insert_section_with_endnote(doc, "Section 2", "Endnote 2, will be pushed down to section 3")
    self.insert_section_with_endnote(doc, "Section 3", "Endnote 3, will stay in section 3")

    # While getting sections to display their respective endnotes, we can set the "suppress_endnotes" flag
    # of a section's "page_setup" object to "True" to revert to the default behavior and pass its endnotes
    # onto the next section.
    page_setup = doc.sections[1].page_setup
    page_setup.suppress_endnotes = True

    doc.save(ARTIFACTS_DIR + "PageSetup.suppress_endnotes.docx")

def insert_section_with_endnote(self, doc: aw.Document, section_body_text: str, endnote_text: str):
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

