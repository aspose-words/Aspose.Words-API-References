---
title: Document.sections property
linktitle: sections property
articleTitle: sections property
second_title: Aspose.Words for Python
description: "Document.sections property. Returns a collection that represents all sections in the document."
type: docs
weight: 380
url: /python-net/aspose.words/document/sections/
---

## Document.sections property

Returns a collection that represents all sections in the document.


```python
@property
def sections(self) -> aspose.words.SectionCollection:
    ...

```

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

Shows how to add and remove sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.write("Section 1")
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write("Section 2")

self.assertEqual("Section 1\u000cSection 2", doc.get_text().strip())

# Delete the first section from the document.
doc.sections.remove_at(0)

self.assertEqual("Section 2", doc.get_text().strip())

# Append a copy of what is now the first section to the end of the document.
last_section_idx = doc.sections.count - 1
new_section = doc.sections[last_section_idx].clone()
doc.sections.add(new_section)

self.assertEqual("Section 2\u000cSection 2", doc.get_text().strip())
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

