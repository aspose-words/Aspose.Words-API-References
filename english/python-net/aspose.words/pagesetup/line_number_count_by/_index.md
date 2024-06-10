---
title: PageSetup.line_number_count_by property
linktitle: line_number_count_by property
articleTitle: line_number_count_by property
second_title: Aspose.Words for Python
description: "PageSetup.line_number_count_by property. Returns or sets the numeric increment for line numbers."
type: docs
weight: 210
url: /python-net/aspose.words/pagesetup/line_number_count_by/
---

## PageSetup.line_number_count_by property

Returns or sets the numeric increment for line numbers.


```python
@property
def line_number_count_by(self) -> int:
    ...

@line_number_count_by.setter
def line_number_count_by(self, value: int):
    ...

```

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
page_setup.line_number_distance_from_text = 50.0
for i in range(1, 26):
    builder.writeln(f'Line {i}.')
# The line counter will skip any paragraph with the "suppress_line_numbers" flag set to "True".
# This paragraph is on the 15th line, which is a multiple of 3, and thus would normally display a line number.
# The section's line counter will also ignore this line, treat the next line as the 15th,
# and continue the count from that point onward.
doc.first_section.body.paragraphs[14].paragraph_format.suppress_line_numbers = True
doc.save(ARTIFACTS_DIR + 'PageSetup.line_numbers.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

