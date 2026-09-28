---
title: Document.last_section property
linktitle: last_section property
articleTitle: last_section property
second_title: Aspose.Words for Python
description: "Document.last_section property. Gets the last section in the document."
type: docs
weight: 250
url: /fr/python-net/aspose.words/document/last_section/
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
# Un document vierge contient une section par défaut,
# qui contient des nœuds enfants que nous pouvons modifier.
self.assertEqual(1, doc.sections.count)
# Utilisez un constructeur de document pour ajouter du texte à la première section.
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Hello world!')
# Créez une deuxième section en insérant un saut de section.
builder.insert_break(aw.BreakType.SECTION_BREAK_NEW_PAGE)
self.assertEqual(2, doc.sections.count)
# Chaque section possède ses propres paramètres de mise en page.
# Nous pouvons diviser le texte de la deuxième section en deux colonnes.
# Cela n'affectera pas le texte de la première section.
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

