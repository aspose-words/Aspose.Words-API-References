---
title: TxtLoadOptions.trailing_spaces_options property
linktitle: trailing_spaces_options property
articleTitle: trailing_spaces_options property
second_title: Aspose.Words for Python
description: "TxtLoadOptions.trailing_spaces_options property. Gets or sets preferred option of a trailing space handling"
type: docs
weight: 70
url: /python-net/aspose.words.loading/txtloadoptions/trailing_spaces_options/
---

## TxtLoadOptions.trailing_spaces_options property

Gets or sets preferred option of a trailing space handling.
Default value is [TxtTrailingSpacesOptions.TRIM](../../txttrailingspacesoptions/#TRIM).



```python
@property
def trailing_spaces_options(self) -> aspose.words.loading.TxtTrailingSpacesOptions:
    ...

@trailing_spaces_options.setter
def trailing_spaces_options(self, value: aspose.words.loading.TxtTrailingSpacesOptions):
    ...

```

### Examples

Shows how to trim whitespace when loading plaintext documents.

```python
text_doc = '      Line 1 \n' + '    Line 2   \n' + ' Line 3       '
# Create a "TxtLoadOptions" object, which we can pass to a document's constructor
# to modify how we load a plaintext document.
load_options = aw.loading.TxtLoadOptions()
# Set the "leading_spaces_options" property to "TxtLeadingSpacesOptions.PRESERVE"
# to preserve all whitespace characters at the start of every line.
# Set the "leading_spaces_options" property to "TxtLeadingSpacesOptions.CONVERT_TO_INDENT"
# to remove all whitespace characters from the start of every line,
# and then apply a left first line indent to the paragraph to simulate the effect of the whitespaces.
# Set the "leading_spaces_options" property to "TxtLeadingSpacesOptions.TRIM"
# to remove all whitespace characters from every line's start.
load_options.leading_spaces_options = txt_leading_spaces_options
# Set the "trailing_spaces_options" property to "TxtTrailingSpacesOptions.PRESERVE"
# to preserve all whitespace characters at the end of every line.
# Set the "trailing_spaces_options" property to "TxtTrailingSpacesOptions.TRIM" to
# remove all whitespace characters from the end of every line.
load_options.trailing_spaces_options = txt_trailing_spaces_options
doc = aw.Document(io.BytesIO(text_doc.encode('utf-8')), load_options)
paragraphs = doc.first_section.body.paragraphs
if txt_leading_spaces_options == aw.loading.TxtLeadingSpacesOptions.CONVERT_TO_INDENT:
    self.assertEqual(37.8, paragraphs[0].paragraph_format.first_line_indent)
    self.assertEqual(25.2, paragraphs[1].paragraph_format.first_line_indent)
    self.assertEqual(6.3, paragraphs[2].paragraph_format.first_line_indent)
    self.assertTrue(paragraphs[0].get_text().startswith('Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith('Line 3'))
elif txt_leading_spaces_options == aw.loading.TxtLeadingSpacesOptions.PRESERVE:
    self.assertTrue(all((p.as_paragraph().paragraph_format.first_line_indent == 0.0 for p in paragraphs)))
    self.assertTrue(paragraphs[0].get_text().startswith('      Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('    Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith(' Line 3'))
elif txt_leading_spaces_options == aw.loading.TxtLeadingSpacesOptions.TRIM:
    self.assertTrue(all((p.as_paragraph().paragraph_format.first_line_indent == 0.0 for p in paragraphs)))
    self.assertTrue(paragraphs[0].get_text().startswith('Line 1'))
    self.assertTrue(paragraphs[1].get_text().startswith('Line 2'))
    self.assertTrue(paragraphs[2].get_text().startswith('Line 3'))
if txt_trailing_spaces_options == aw.loading.TxtTrailingSpacesOptions.PRESERVE:
    self.assertTrue(paragraphs[0].get_text().endswith('Line 1 \r'))
    self.assertTrue(paragraphs[1].get_text().endswith('Line 2   \r'))
    self.assertTrue(paragraphs[2].get_text().endswith('Line 3       \x0c'))
elif txt_trailing_spaces_options == aw.loading.TxtTrailingSpacesOptions.TRIM:
    self.assertTrue(paragraphs[0].get_text().endswith('Line 1\r'))
    self.assertTrue(paragraphs[1].get_text().endswith('Line 2\r'))
    self.assertTrue(paragraphs[2].get_text().endswith('Line 3\x0c'))
```

### See Also

* module [aspose.words.loading](../../)
* class [TxtLoadOptions](../)

