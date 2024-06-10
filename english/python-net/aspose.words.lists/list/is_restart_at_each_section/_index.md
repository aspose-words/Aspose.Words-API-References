---
title: List.is_restart_at_each_section property
linktitle: is_restart_at_each_section property
articleTitle: is_restart_at_each_section property
second_title: Aspose.Words for Python
description: "List.is_restart_at_each_section property. Specifies whether list should be restarted at each section"
type: docs
weight: 50
url: /python-net/aspose.words.lists/list/is_restart_at_each_section/
---

## List.is_restart_at_each_section property

Specifies whether list should be restarted at each section.
Default value is ``False``.



```python
@property
def is_restart_at_each_section(self) -> bool:
    ...

@is_restart_at_each_section.setter
def is_restart_at_each_section(self, value: bool):
    ...

```

### Remarks

This option is supported only in RTF, DOC and DOCX document formats.

This option will be written to DOCX only if [OoxmlCompliance](../../../aspose.words.saving/ooxmlcompliance/) is higher then [OoxmlCompliance.ECMA376_2006](../../../aspose.words.saving/ooxmlcompliance/#ECMA376_2006).




### Examples

Shows how to configure a list to restart numbering at each section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
doc.lists.add(aw.lists.ListTemplate.NUMBER_DEFAULT)
list = doc.lists[0]
list.is_restart_at_each_section = restart_list_at_each_section
# The "is_restart_at_each_section" property will only be applicable when
# the document's OOXML compliance level is to a standard that is newer than "OoxmlComplianceCore.ECMA376".
options = aw.saving.OoxmlSaveOptions()
options.compliance = aw.saving.OoxmlCompliance.ISO29500_2008_TRANSITIONAL
builder.list_format.list = list
builder.writeln('List item 1')
builder.writeln('List item 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.writeln('List item 3')
builder.writeln('List item 4')
doc.save(ARTIFACTS_DIR + 'OoxmlSaveOptions.restarting_document_list.docx', options)
doc = aw.Document(ARTIFACTS_DIR + 'OoxmlSaveOptions.restarting_document_list.docx')
self.assertEqual(restart_list_at_each_section, doc.lists[0].is_restart_at_each_section)
```

### See Also

* module [aspose.words.lists](../../)
* class [List](../)

