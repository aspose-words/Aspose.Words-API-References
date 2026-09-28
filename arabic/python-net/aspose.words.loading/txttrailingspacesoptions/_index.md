---
title: TxtTrailingSpacesOptions enumeration
linktitle: TxtTrailingSpacesOptions enumeration
articleTitle: TxtTrailingSpacesOptions enumeration
second_title: Aspose.Words for Python
description: "aspose.words.loading.TxtTrailingSpacesOptions enumeration. Specifies available options for trailing spaces handling during import from [LoadFormat.TEXT](../../aspose.words/loadformat/#TEXT) file."
type: docs
weight: 210
url: /ar/python-net/aspose.words.loading/txttrailingspacesoptions/
---

## TxtTrailingSpacesOptions enumeration

Specifies available options for trailing spaces handling during import from [LoadFormat.TEXT](../../aspose.words/loadformat/#TEXT) file.



### Members

| Name | Description |
| --- | --- |
| TRIM | Trailing spaces are trimmed. |
| PRESERVE | Trailing spaces are preserved. |

### Examples

Shows how to trim whitespace when loading plaintext documents.

```python
text_doc = '      Line 1 \n' + '    Line 2   \n' + ' Line 3       '
# أنشئ كائن "TxtLoadOptions"، الذي يمكننا تمريره إلى مُنشئ المستند
# لتعديل طريقة تحميل مستند نص عادي.
load_options = aw.loading.TxtLoadOptions()
# قم بتعيين خاصية "LeadingSpacesOptions" إلى "TxtLeadingSpacesOptions.Preserve"
# للحفاظ على جميع مسافات الفراغ في بداية كل سطر.
# قم بتعيين خاصية "LeadingSpacesOptions" إلى "TxtLeadingSpacesOptions.ConvertToIndent"
# لإزالة جميع مسافات الفراغ من بداية كل سطر،
# ثم تطبيق مسافة بادئة للخط الأول إلى اليسار على الفقرة لمحاكاة تأثير الفراغات.
# قم بتعيين خاصية "LeadingSpacesOptions" إلى "TxtLeadingSpacesOptions.Trim"
# لإزالة جميع أحرف المسافات البيضاء من بداية كل سطر.
load_options.leading_spaces_options = txt_leading_spaces_options
# اضبط خاصية "TrailingSpacesOptions" إلى "TxtTrailingSpacesOptions.Preserve"
# للحفاظ على جميع أحرف المسافات البيضاء في نهاية كل سطر.
# اضبط خاصية "TrailingSpacesOptions" إلى "TxtTrailingSpacesOptions.Trim" لت
# إزالة جميع أحرف المسافات البيضاء من نهاية كل سطر.
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

* module [aspose.words.loading](../)

