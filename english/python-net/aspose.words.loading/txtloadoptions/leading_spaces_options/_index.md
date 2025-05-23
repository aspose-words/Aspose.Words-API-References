﻿---
title: TxtLoadOptions.leading_spaces_options property
linktitle: leading_spaces_options property
articleTitle: leading_spaces_options property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.leading_spaces_options property. Gets or sets preferred option of a leading space handling"
type: docs
weight: 60
url: /python-net/aspose.words.loading/txtloadoptions/leading_spaces_options/
---

## TxtLoadOptions.leading_spaces_options property

Gets or sets preferred option of a leading space handling.
Default value is [TxtLeadingSpacesOptions.CONVERT_TO_INDENT](../../txtleadingspacesoptions/#CONVERT_TO_INDENT).



```python
@property
def leading_spaces_options(self) -> aspose.words.loading.TxtLeadingSpacesOptions:
    ...

@leading_spaces_options.setter
def leading_spaces_options(self, value: aspose.words.loading.TxtLeadingSpacesOptions):
    ...

```

### Examples

Shows how to trim whitespace when loading plaintext documents.

```python
text_doc = '      Line 1 \n' + '    Line 2   \n' + ' Line 3       '
# Create a "TxtLoadOptions" object, which we can pass to a document's constructor
# to modify how we load a plaintext document.
load_options = aw.loading.TxtLoadOptions()
# Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Preserve"
# to preserve all whitespace characters at the start of every line.
# Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.ConvertToIndent"
# to remove all whitespace characters from the start of every line,
# and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
# Set the "LeadingSpacesOptions" property to "TxtLeadingSpacesOptions.Trim"
# to remove all whitespace characters from every line's start.
load_options.leading_spaces_options = txt_leading_spaces_options
# Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Preserve"
# to preserve all whitespace characters at the end of every line.
# Set the "TrailingSpacesOptions" property to "TxtTrailingSpacesOptions.Trim" to
# remove all whitespace characters from the end of every line.
load_options.trailing_spaces_options = txt_trailing_spaces_options
doc = aw.Document(stream=io.BytesIO(system_helper.text.Encoding.get_bytes(text_doc, system_helper.text.Encoding.utf_8())), load_options=load_options)
paragraphs = doc.first_section.body.paragraphs
switch_condition = txt_leading_spaces_options
if switch_condition == aw.loading.TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
    self.assertEqual(37.8, paragraphs[0].paragraph_format.first_line_indent)
    self.assertEqual(25.2, paragraphs[1].paragraph_format.first_line_indent)
    self.assertEqual(6.3, paragraphs[2].paragraph_format.first_line_indent)
    self.assertTrue(paragraphs[0].get_text().startswith('Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith('Line 3'))
elif switch_condition == aw.loading.TxtLeadingSpacesOptions.PRESERVE:
    self.assertTrue(all([p.as_paragraph().paragraph_format.first_line_indent == 0 for p in paragraphs]))
    self.assertTrue(paragraphs[0].get_text().startswith('      Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('    Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith(' Line 3'))
elif switch_condition == aw.loading.TxtLeadingSpacesOptions.TRIM:
    self.assertTrue(all([p.as_paragraph().paragraph_format.first_line_indent == 0 for p in paragraphs]))
    self.assertTrue(paragraphs[0].get_text().startswith('Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith('Line 3'))
switch_condition = txt_trailing_spaces_options
if switch_condition == aw.loading.TxtTrailingSpacesOptions.PRESERVE:
    self.assertTrue(paragraphs[0].get_text().endswith('Line 1 \r'))
    self.assertTrue(paragraphs[1].get_text().endswith('Line 2   \r'))
    self.assertTrue(paragraphs[2].get_text().endswith('Line 3       \x0c'))
elif switch_condition == aw.loading.TxtTrailingSpacesOptions.TRIM:
    self.assertTrue(paragraphs[0].get_text().endswith('Line 1\r'))
    self.assertTrue(paragraphs[1].get_text().endswith('Line 2\r'))
    self.assertTrue(paragraphs[2].get_text().endswith('Line 3\x0c'))
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

