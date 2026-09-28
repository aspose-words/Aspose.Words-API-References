---
title: FieldCitation.format_language_id property
linktitle: format_language_id property
articleTitle: format_language_id property
second_title: Aspose.Words for Python
description: "FieldCitation.format_language_id property. Gets or sets the language ID that is used in conjunction with the specified bibliographic style to format the citation in the document."
type: docs
weight: 30
url: /fr/python-net/aspose.words.fields/fieldcitation/format_language_id/
---

## FieldCitation.format_language_id property

Gets or sets the language ID that is used in conjunction with the specified bibliographic style to format the citation
in the document.


```python
@property
def format_language_id(self) -> str:
    ...

@format_language_id.setter
def format_language_id(self, value: str):
    ...

```

### Examples

Shows how to work with CITATION and BIBLIOGRAPHY fields.

```python
# Ouvrez un document contenant des sources bibliographiques que nous pouvons trouver dans
# Microsoft Word via Références -> Citations & Bibliographie -> Gérer les sources.
doc = aw.Document(MY_DIR + 'Bibliography.docx')
builder = aw.DocumentBuilder(doc)
builder.write('Text to be cited with one source.')
# Créez une citation avec uniquement le numéro de page et l'auteur du livre référencé.
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
# Nous faisons référence aux sources en utilisant leurs noms d'étiquette.
field_citation.source_tag = 'Book1'
field_citation.page_number = '85'
field_citation.suppress_author = False
field_citation.suppress_title = True
field_citation.suppress_year = True
self.assertEqual(' CITATION  Book1 \\p 85 \\t \\y', field_citation.get_field_code())
# Créez une citation plus détaillée qui cite deux sources.
builder.insert_paragraph()
builder.write('Text to be cited with two sources.')
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
field_citation.source_tag = 'Book1'
field_citation.another_source_tag = 'Book2'
field_citation.format_language_id = 'en-US'
field_citation.page_number = '19'
field_citation.prefix = 'Prefix '
field_citation.suffix = ' Suffix'
field_citation.suppress_author = False
field_citation.suppress_title = False
field_citation.suppress_year = False
field_citation.volume_number = 'VII'
self.assertEqual(' CITATION  Book1 \\m Book2 \\l en-US \\p 19 \\f "Prefix " \\s " Suffix" \\v VII', field_citation.get_field_code())
# Nous pouvons utiliser un champ BIBLIOGRAPHY pour afficher toutes les sources du document.
builder.insert_break(aw.BreakType.PAGE_BREAK)
field_bibliography = builder.insert_field(aw.fields.FieldType.FIELD_BIBLIOGRAPHY, True).as_field_bibliography()
field_bibliography.format_language_id = '5129'
self.assertEqual(' BIBLIOGRAPHY  \\l 5129', field_bibliography.get_field_code())
doc.update_fields()
doc.save(ARTIFACTS_DIR + 'Field.field_citation.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldCitation](../)

