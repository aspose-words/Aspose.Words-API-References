---
title: Document.first_section property
linktitle: first_section property
articleTitle: first_section property
second_title: Aspose.Words for Python
description: "Document.first_section property. Gets the first section in the document."
type: docs
weight: 140
url: /python-net/aspose.words/document/first_section/
---

## Document.first_section property

Gets the first section in the document.


```python
@property
def first_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to replace text in a document's footer.

```python
doc = aw.Document(MY_DIR + 'Footer.docx')
headers_footers = doc.first_section.headers_footers
footer = headers_footers.get_by_header_footer_type(aw.HeaderFooterType.FOOTER_PRIMARY)
options = aw.replacing.FindReplaceOptions()
options.match_case = False
options.find_whole_words_only = False
current_year = date.today().year
footer.range.replace('(C) 2006 Aspose Pty Ltd.', f'Copyright (C) {current_year} by Aspose Pty Ltd.', options)
doc.save(ARTIFACTS_DIR + 'HeaderFooter.replace_text.docx')
```

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# A blank document contains one section by default,
# which contains child nodes that we can edit.
self.assertEqual(1, doc.sections.count)
# Use a document builder to add text to the first section.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Create a second section by inserting a section break.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# Each section has its own page setup settings.
# We can split the text in the second section into two columns.
# This will not affect the text in the first section.
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

