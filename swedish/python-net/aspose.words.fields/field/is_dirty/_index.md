---
title: Field.is_dirty property
linktitle: is_dirty property
articleTitle: is_dirty property
second_title: Aspose.Words for Python
description: "Field.is_dirty property. Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document."
type: docs
weight: 40
url: /sv/python-net/aspose.words.fields/field/is_dirty/
---

## Field.is_dirty property

Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.


```python
@property
def is_dirty(self) -> bool:
    ...

@is_dirty.setter
def is_dirty(self, value: bool):
    ...

```

### Examples

Shows how to use special property for updating field result.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ge dokumentets inbyggda "Author"-egenskapsvärde och visa det sedan med ett fält.
doc.built_in_document_properties.author = 'John Doe'
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTHOR, update_field=True).as_field_author()
self.assertFalse(field.is_dirty)
self.assertEqual('John Doe', field.result)
# Uppdatera egenskapen. Fältet visar fortfarande det gamla värdet.
doc.built_in_document_properties.author = 'John & Jane Doe'
self.assertEqual('John Doe', field.result)
# Eftersom fältets värde är föråldrat kan vi markera det som "dirty".
# Detta värde kommer att förbli föråldrat tills vi uppdaterar fältet manuellt med metoden Field.Update().
field.is_dirty = True
with io.BytesIO() as doc_stream:
    # Om vi sparar utan att anropa en uppdateringsmetod,
    # kommer fältet fortsätta att visa det föråldrade värdet i utdata-dokumentet.
    doc.save(stream=doc_stream, save_format=aw.SaveFormat.DOCX)
    # LoadOptions-objektet har ett alternativ för att uppdatera alla fält
    # markerade som "dirty" när dokumentet läses in.
    options = aw.loading.LoadOptions()
    options.update_dirty_fields = update_dirty_fields
    doc = aw.Document(stream=doc_stream, load_options=options)
    self.assertEqual('John & Jane Doe', doc.built_in_document_properties.author)
    field = doc.range.fields[0].as_field_author()
    # Att uppdatera "dirty"-fält på detta sätt sätter automatiskt deras "IsDirty"-flagga till falskt.
    if update_dirty_fields:
        self.assertEqual('John & Jane Doe', field.result)
        self.assertFalse(field.is_dirty)
    else:
        self.assertEqual('John Doe', field.result)
        self.assertTrue(field.is_dirty)
```

### See Also

* module [aspose.words.fields](../../)
* class [Field](../)

