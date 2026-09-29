---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 250
url: /sv/python-net/aspose.words/document/last_section/
---

## Document.last_section property

Gets the last section in the document.


```python
@property
def last_section(self) -> aspose.words.Section:
    ...

```

### Remarks

Returns ``None`` if there are no sections.



### Examples

Shows how to create a new section with a document builder.

```python
doc = aw.Document()
# Ett tomt dokument innehåller som standard en sektion,
# som innehåller undernoder som vi kan redigera.
self.assertEqual(1, doc.sections.count)
# Använd en dokumentbyggare för att lägga till text i den första sektionen.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Skapa en andra sektion genom att infoga en sektionsbrytning.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# Varje sektion har sina egna sidinställningar.
# Vi kan dela upp texten i den andra sektionen i två kolumner.
# Detta kommer inte att påverka texten i den första sektionen.
doc.last_section.page_setup.text_columns.set_count(2)
builder.writeln('Column 1.')
builder.insert_break(aw.BreakType.COLUMN_BREAK)
builder.writeln('Column 2.')
self.assertEqual(1, doc.first_section.page_setup.text_columns.count)
self.assertEqual(2, doc.last_section.page_setup.text_columns.count)
doc.save(file_name=ARTIFACTS_DIR + 'Section.Create.docx')
```

### See Also

* module [aspose.words](../../)
* class [Document](../)

