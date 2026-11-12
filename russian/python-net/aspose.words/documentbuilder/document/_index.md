---
title: DocumentBuilder.document property
linktitle: document property
articleTitle: document property
second_title: Aspose.Words for Python
description: "DocumentBuilder.document property. Gets or sets the [DocumentBuilder.document](./) object that this object is attached to."
type: docs
weight: 90
url: /ru/python-net/aspose.words/documentbuilder/document/
---

## DocumentBuilder.document property

Gets or sets the [DocumentBuilder.document](./) object that this object is attached to.



```python
@property
def document(self) -> aspose.words.Document:
    ...

@document.setter
def document(self, value: aspose.words.Document):
    ...

```

### Examples

Shows how to apply and revert page setup settings to sections in a document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Измените свойства настройки страницы для текущего раздела построителя и добавьте текст.
builder.page_setup.orientation = aw.Orientation.LANDSCAPE
builder.page_setup.vertical_alignment = aw.PageVerticalAlignment.CENTER
builder.writeln('This is the first section, which landscape oriented with vertically centered text.')
# Если мы начнём новый раздел, используя DocumentBuilder,
# он унаследует текущие свойства настройки страницы построителя.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(aw.Orientation.LANDSCAPE, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.CENTER, doc.sections[1].page_setup.vertical_alignment)
# Мы можем вернуть его свойства настройки страницы к значениям по умолчанию, используя метод "ClearFormatting".
builder.page_setup.clear_formatting()
self.assertEqual(aw.Orientation.PORTRAIT, doc.sections[1].page_setup.orientation)
self.assertEqual(aw.PageVerticalAlignment.TOP, doc.sections[1].page_setup.vertical_alignment)
builder.writeln('This is the second section, which is in default Letter paper size, portrait orientation and top alignment.')
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.ClearFormatting.docx')
```

### See Also

* module [aspose.words](../../)
* class [DocumentBuilder](../)

