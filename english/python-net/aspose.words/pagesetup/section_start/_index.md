---
title: PageSetup.section_start property
linktitle: section_start property
articleTitle: section_start property
second_title: Aspose.Words for Python
description: "PageSetup.section_start property. Returns or sets the type of section break for the specified object."
type: docs
weight: 390
url: /python-net/aspose.words/pagesetup/section_start/
---

## PageSetup.section_start property

Returns or sets the type of section break for the specified object.


### Examples

Shows how to specify how a new section separates itself from the previous.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln("This text is in section 1.")

# Section break types determine how a new section separates itself from the previous section.
# Below are five types of section breaks.
# 1 -  Starts the next section on a new page:
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln("This text is in section 2.")

self.assertEqual(aw.SectionStart.NEW_PAGE, doc.sections[1].page_setup.section_start)

# 2 -  Starts the next section on the current page:
builder.insert_break(aw.BreakType.SECTION_BREAK_CONTINUOUS)
builder.writeln("This text is in section 3.")

self.assertEqual(aw.SectionStart.CONTINUOUS, doc.sections[2].page_setup.section_start)

# 3 -  Starts the next section on a new even page:
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.writeln("This text is in section 4.")

self.assertEqual(aw.SectionStart.EVEN_PAGE, doc.sections[3].page_setup.section_start)

# 4 -  Starts the next section on a new odd page:
builder.insert_break(aw.BreakType.SECTION_BREAK_ODD_PAGE)
builder.writeln("This text is in section 5.")

self.assertEqual(aw.SectionStart.ODD_PAGE, doc.sections[4].page_setup.section_start)

# 5 -  Starts the next section on a new column:
columns = builder.page_setup.text_columns
columns.set_count(2)

builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_COLUMN)
builder.writeln("This text is in section 6.")

self.assertEqual(aw.SectionStart.NEW_COLUMN, doc.sections[5].page_setup.section_start)

doc.save(ARTIFACTS_DIR + "PageSetup.set_section_start.docx")
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
* class [PageSetup](../)

