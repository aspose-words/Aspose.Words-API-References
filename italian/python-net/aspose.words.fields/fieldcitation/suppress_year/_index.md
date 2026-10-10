---
title: FieldCitation.suppress_year property
linktitle: suppress_year property
articleTitle: suppress_year property
second_title: Aspose.Words for Python
description: "FieldCitation.suppress_year property. Gets or sets whether the year information is suppressed from the citation."
type: docs
weight: 100
url: /it/python-net/aspose.words.fields/fieldcitation/suppress_year/
---

## FieldCitation.suppress_year property

Gets or sets whether the year information is suppressed from the citation.


```python
@property
def suppress_year(self) -> bool:
    ...

@suppress_year.setter
def suppress_year(self, value: bool):
    ...

```

### Examples

Shows how to work with CITATION and BIBLIOGRAPHY fields.

```python
# Apri un documento contenente fonti bibliografiche che possiamo trovare in
# Microsoft Word tramite Riferimenti -> Citazioni e Bibliografia -> Gestisci fonti.
doc = aw.Document(MY_DIR + 'Bibliography.docx')
builder = aw.DocumentBuilder(doc)
builder.write('Text to be cited with one source.')
# Crea una citazione con solo il numero di pagina e l'autore del libro di riferimento.
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
# Facciamo riferimento alle fonti usando i loro nomi di tag.
field_citation.source_tag = 'Book1'
field_citation.page_number = '85'
field_citation.suppress_author = False
field_citation.suppress_title = True
field_citation.suppress_year = True
self.assertEqual(' CITATION  Book1 \\p 85 \\t \\y', field_citation.get_field_code())
# Crea una citazione più dettagliata che cita due fonti.
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
# Possiamo usare un campo BIBLIOGRAPHY per visualizzare tutte le fonti all'interno del documento.
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

