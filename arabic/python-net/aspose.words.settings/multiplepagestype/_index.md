---
title: MultiplePagesType enumeration
linktitle: MultiplePagesType enumeration
articleTitle: MultiplePagesType enumeration
second_title: Aspose.Words for Python
description: "aspose.words.settings.MultiplePagesType enumeration. Specifies how document is printed out."
type: docs
weight: 110
url: /ar/python-net/aspose.words.settings/multiplepagestype/
---

## MultiplePagesType enumeration

Specifies how document is printed out.


### Members

| Name | Description |
| --- | --- |
| NORMAL | Normal printing, no multiple pages specified. |
| MIRROR_MARGINS | Swaps left and right margins on facing pages. |
| TWO_PAGES_PER_SHEET | Prints two pages per sheet. |
| BOOK_FOLD_PRINTING | Specifies whether to print the document as a book fold. |
| BOOK_FOLD_PRINTING_REVERSE | Specifies whether to print the document as a reverse book fold. |
| DEFAULT | Default value is [MultiplePagesType.NORMAL](./#NORMAL) |

### Examples

Shows how to configure a document that can be printed as a book fold.

```python
doc = aw.Document()
# أدرج نصًا يمتد عبر 16 صفحة.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('My Booklet:')
i = 0
while i < 15:
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    builder.write(f'Booklet face #{i}')
    i += 1
# قم بتكوين خاصية "PageSetup" للقسم الأول لطباعة المستند على شكل طية كتاب.
# عند طباعة هذا المستند على الوجهين، يمكننا أخذ الصفحات لتكديسها
# وطويها جميعًا من الوسط مرة واحدة. سيُرتّب محتوى المستند في طية كتاب.
page_setup = doc.sections[0].page_setup
page_setup.multiple_pages = aw.settings.MultiplePagesType.BOOK_FOLD_PRINTING
# يمكننا تحديد عدد الأوراق فقط على أساس مضاعفات 4.
page_setup.sheets_per_booklet = 4
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Booklet.docx')
```

### See Also

* module [aspose.words.settings](../)

