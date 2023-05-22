---
title: ParagraphFormat.alignment property
linktitle: alignment property
articleTitle: alignment property
second_title: Aspose.Words for Python
description: "ParagraphFormat.alignment property. Gets or sets text alignment for the paragraph."
type: docs
weight: 30
url: /python-net/aspose.words/paragraphformat/alignment/
---

## ParagraphFormat.alignment property

Gets or sets text alignment for the paragraph.


### Examples

Shows how to insert a paragraph into the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

font = builder.font
font.size = 16
font.bold = True
font.color = drawing.Color.blue
font.name = "Arial"
font.underline = aw.Underline.DASH

paragraph_format = builder.paragraph_format
paragraph_format.first_line_indent = 8
paragraph_format.alignment = aw.ParagraphAlignment.JUSTIFY
paragraph_format.add_space_between_far_east_and_alpha = True
paragraph_format.add_space_between_far_east_and_digit = True
paragraph_format.keep_together = True

# The "writeln" method ends the paragraph after appending text
# and then starts a new line, adding a new paragraph.
builder.writeln("Hello world!")

self.assertTrue(builder.current_paragraph.is_end_of_document)
```

Shows how to construct an Aspose.Words document by hand.

```python
doc = aw.Document()

# A blank document contains one section, one body and one paragraph.
# Call the "remove_all_children" method to remove all those nodes,
# and end up with a document node with no children.
doc.remove_all_children()

# This document now has no composite child nodes that we can add content to.
# If we wish to edit it, we will need to repopulate its node collection.
# First, create a new section, and then append it as a child to the root document node.
section = aw.Section(doc)
doc.append_child(section)

# Set some page setup properties for the section.
section.page_setup.section_start = aw.SectionStart.NEW_PAGE
section.page_setup.paper_size = aw.PaperSize.LETTER

# A section needs a body, which will contain and display all its contents
# on the page between the section's header and footer.
body = aw.Body(doc)
section.append_child(body)

# Create a paragraph, set some formatting properties, and then append it as a child to the body.
para = aw.Paragraph(doc)

para.paragraph_format.style_name = "Heading 1"
para.paragraph_format.alignment = aw.ParagraphAlignment.CENTER

body.append_child(para)

# Finally, add some content to do the document. Create a run,
# set its appearance and contents, and then append it as a child to the paragraph.
run = aw.Run(doc)
run.text = "Hello World!"
run.font.color = drawing.Color.red
para.append_child(run)

self.assertEqual("Hello World!", doc.get_text().strip())

doc.save(ARTIFACTS_DIR + "Section.create_manually.docx")
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

