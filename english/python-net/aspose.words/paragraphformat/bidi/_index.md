---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 40
url: /python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# The BIDIOUTLINE field numbers paragraphs like the AUTONUM/LISTNUM fields,
# but is only visible when a right-to-left editing language is enabled, such as Hebrew or Arabic.
# The following field will display ".1", the RTL equivalent of list number "1.".
field = builder.insert_field(aw.fields.FieldType.FIELD_BIDI_OUTLINE, True).as_field_bidi_outline()
builder.writeln("שלום")

self.assertEqual(" BIDIOUTLINE ", field.get_field_code())

# Add two more BIDIOUTLINE fields, which will display ".2" and ".3".
builder.insert_field(aw.fields.FieldType.FIELD_BIDI_OUTLINE, True)
builder.writeln("שלום")
builder.insert_field(aw.fields.FieldType.FIELD_BIDI_OUTLINE, True)
builder.writeln("שלום")

# Set the horizontal text alignment for every paragraph in the document to RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True

# If we enable a right-to-left editing language in Microsoft Word, our fields will display numbers.
# Otherwise, they will display "###".
doc.save(ARTIFACTS_DIR + "Field.field_bidi_outline.docx")
```

Shows how to detect plaintext document text direction.

```python
# Create a "TxtLoadOptions" object, which we can pass to a document's constructor
# to modify how we load a plaintext document.
load_options = aw.loading.TxtLoadOptions()

# Set the "document_direction" property to "DocumentDirection.AUTO" automatically detects
# the direction of every paragraph of text that Aspose.Words loads from plaintext.
# Each paragraph's "bidi" property will store its direction.
load_options.document_direction = aw.loading.DocumentDirection.AUTO

# Detect Hebrew text as right-to-left.
doc = aw.Document(MY_DIR + "Hebrew text.txt", load_options)

self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)

# Detect English text as right-to-left.
doc = aw.Document(MY_DIR + "English text.txt", load_options)

self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

