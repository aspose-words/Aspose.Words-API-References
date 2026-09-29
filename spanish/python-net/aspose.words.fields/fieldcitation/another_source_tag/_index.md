---
title: FieldCitation.another_source_tag property
linktitle: another_source_tag property
articleTitle: another_source_tag property
second_title: Aspose.Words for Python
description: "FieldCitation.another_source_tag property. Gets or sets a value that matches the Tag element's value of another source to be included in the citation."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldcitation/another_source_tag/
---

## FieldCitation.another_source_tag property

Gets or sets a value that matches the **Tag** element's value of another source to be included in the citation.



```python
@property
def another_source_tag(self) -> str:
    ...

@another_source_tag.setter
def another_source_tag(self, value: str):
    ...

```

### Examples

Shows how to work with CITATION and BIBLIOGRAPHY fields.

```python
# Abra un documento que contenga fuentes bibliográficas que podemos encontrar en
# Microsoft Word a través de Referencias -> Citas y Bibliografía -> Administrar fuentes.
doc = aw.Document(MY_DIR + 'Bibliography.docx')
builder = aw.DocumentBuilder(doc)
builder.write('Text to be cited with one source.')
# Cree una cita solo con el número de página y el autor del libro referenciado.
field_citation = builder.insert_field(aw.fields.FieldType.FIELD_CITATION, True).as_field_citation()
# Nos referimos a las fuentes usando sus nombres de etiqueta.
field_citation.source_tag = 'Book1'
field_citation.page_number = '85'
field_citation.suppress_author = False
field_citation.suppress_title = True
field_citation.suppress_year = True
self.assertEqual(' CITATION  Book1 \\p 85 \\t \\y', field_citation.get_field_code())
# Crea una cita más detallada que cite dos fuentes.
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
# Podemos usar un campo BIBLIOGRAPHY para mostrar todas las fuentes dentro del documento.
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

