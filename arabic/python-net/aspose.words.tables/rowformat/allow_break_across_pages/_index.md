---
title: RowFormat.allow_break_across_pages property
linktitle: allow_break_across_pages property
articleTitle: allow_break_across_pages property
second_title: Aspose.Words for Python
description: "RowFormat.allow_break_across_pages property. True if the text in a table row is allowed to split across a page break."
type: docs
weight: 10
url: /ar/python-net/aspose.words.tables/rowformat/allow_break_across_pages/
---

## RowFormat.allow_break_across_pages property

True if the text in a table row is allowed to split across a page break.


```python
@property
def allow_break_across_pages(self) -> bool:
    ...

@allow_break_across_pages.setter
def allow_break_across_pages(self, value: bool):
    ...

```

### Examples

Shows how to disable rows breaking across pages for every row in a table.

```python
doc = aw.Document(file_name=MY_DIR + 'Table spanning two pages.docx')
table = doc.first_section.body.tables[0]
# قم بتعيين الخاصية "AllowBreakAcrossPages" إلى "false" للحفاظ على الصف
# كقطعة واحدة إذا امتد الجدول على صفحتين، مما يسبب انقسامه عند ذلك الصف.
# إذا كان الصف كبيرًا جدًا ليتناسب في صفحة واحدة، سيقوم Microsoft Word بنقله إلى الصفحة التالية.
# قم بتعيين الخاصية "AllowBreakAcrossPages" إلى "true" للسماح للصف بالانقسام عبر صفحتين.
for row in table:
    row = row.as_row()
    row.row_format.allow_break_across_pages = allow_break_across_pages
doc.save(file_name=ARTIFACTS_DIR + 'Table.AllowBreakAcrossPages.docx')
```

### See Also

* module [aspose.words.tables](../../)
* class [RowFormat](../)

