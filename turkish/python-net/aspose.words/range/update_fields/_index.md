---
title: Range.update_fields method
linktitle: update_fields method
articleTitle: update_fields method
second_title: Aspose.Words for Python
description: "Range.update_fields method. Updates the values of document fields in this range."
type: docs
weight: 130
url: /tr/python-net/aspose.words/range/update_fields/
---

## update_fields() {#default}

Updates the values of document fields in this range.


```python
def update_fields(self):
    ...
```

### Remarks

When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact.
Therefore, you would usually want to call this method before saving if you have modified the document
programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update
and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF).
The page layout-related fields are updated when you render a document or call [Document.update_page_layout()](../../document/update_page_layout/#default).

To update fields in the whole document use [Document.update_fields()](../../document/update_fields/#default).




### Examples

Shows how to update all the fields in a range.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.insert_field(field_code=' DOCPROPERTY Category')
builder.insert_break(aw.BreakType.SECTION_BREAK_EVEN_PAGE)
builder.insert_field(field_code=' DOCPROPERTY Category')
# Yukarıdaki DOCPROPERTY alanları, bu yerleşik belge özelliğinin değerini gösterecektir.
doc.built_in_document_properties.category = 'MyCategory'
# Bir belge özelliğinin değerini güncellerseniz, bunu göstermek için tüm DOCPROPERTY alanlarını da güncellemeniz gerekir.
self.assertEqual('', doc.range.fields[0].result)
self.assertEqual('', doc.range.fields[1].result)
# İlk bölüm aralığındaki tüm alanları güncelleyin.
doc.first_section.range.update_fields()
self.assertEqual('MyCategory', doc.range.fields[0].result)
self.assertEqual('', doc.range.fields[1].result)
```

### See Also

* module [aspose.words](../../)
* class [Range](../)

