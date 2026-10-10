---
title: Section.append_content method
linktitle: append_content method
articleTitle: append_content method
second_title: Aspose.Words for Python
description: "Section.append_content method. Inserts a copy of content of the source section at the end of this section."
type: docs
weight: 80
url: /ar/python-net/aspose.words/section/append_content/
---

## append_content(source_section) {#section}

Inserts a copy of content of the source section at the end of this section.


```python
def append_content(self, source_section: aspose.words.Section):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| source_section | [Section](../) | The section to copy content from. |

### Remarks

Only content of [Section.body](../body/) of the source section is copied, page setup,
headers and footers are not copied.

The nodes are automatically imported if the source section belongs to a different document.

No new section is created in the destination document.




### Examples

Shows how to append the contents of a section to another section.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.write('Section 1')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 2')
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
builder.write('Section 3')
section = doc.sections[2]
self.assertEqual('Section 3' + aw.ControlChar.SECTION_BREAK, section.get_text())
# أدرج محتويات القسم الأول في بداية القسم الثالث.
section_to_prepend = doc.sections[0]
section.prepend_content(section_to_prepend)
# أدرج محتويات القسم الثاني في نهاية القسم الثالث.
section_to_append = doc.sections[1]
section.append_content(section_to_append)
# لم تقم طريقتا "PrependContent" و "AppendContent" بإنشاء أي أقسام جديدة.
self.assertEqual(3, doc.sections.count)
self.assertEqual('Section 1' + aw.ControlChar.PARAGRAPH_BREAK + 'Section 3' + aw.ControlChar.PARAGRAPH_BREAK + 'Section 2' + aw.ControlChar.SECTION_BREAK, section.get_text())
```

### See Also

* module [aspose.words](../../)
* class [Section](../)

