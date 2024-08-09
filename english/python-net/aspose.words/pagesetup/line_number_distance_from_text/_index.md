---
title: PageSetup.line_number_distance_from_text property
linktitle: line_number_distance_from_text property
articleTitle: line_number_distance_from_text property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_distance_from_text property. Gets or sets distance between the right edge of line numbers and the left edge of the document."
type: docs
weight: 220
url: /python-net/aspose.words/pagesetup/line_number_distance_from_text/
---

## PageSetup.line_number_distance_from_text property

Gets or sets distance between the right edge of line numbers and the left edge of the document.


```python
@property
def line_number_distance_from_text(self) -> float:
    ...

@line_number_distance_from_text.setter
def line_number_distance_from_text(self, value: float):
    ...

```

### Remarks

Set this property to zero for automatic distance between the line numbers and text of the document.


### Examples

Shows how to enable line numbering for a section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
# We can use the section's PageSetup object to display numbers to the left of the section's text lines.
# This is the same behavior as a List object,
# but it covers the entire section and does not modify the text in any way.
# Our section will restart the numbering on each new page from 1 and display the number,
# if it is a multiple of 3, at 50pt to the left of the line.
page_setup = builder.page_setup
page_setup.line_starting_number = 1
page_setup.line_number_count_by = 3
page_setup.line_number_restart_mode = aw.LineNumberRestartMode.RESTART_PAGE
page_setup.line_number_distance_from_text = 50
i = 1
while i <= 25:
    builder.writeln(f'Line {i}.')
    i += 1
# The line counter will skip any paragraph with the "SuppressLineNumbers" flag set to "true".
# This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
# The section's line counter will also ignore this line, treat the next line as the 15th,
# and continue the count from that point onward.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.LineNumbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

