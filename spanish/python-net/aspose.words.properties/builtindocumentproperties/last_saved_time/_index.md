---
title: BuiltInDocumentProperties.last_saved_time property
linktitle: last_saved_time property
articleTitle: last_saved_time property
second_title: Aspose.Words for Python
description: "BuiltInDocumentProperties.last_saved_time property. Gets or sets the time of the last save in UTC."
type: docs
weight: 180
url: /es/python-net/aspose.words.properties/builtindocumentproperties/last_saved_time/
---

## BuiltInDocumentProperties.last_saved_time property

Gets or sets the time of the last save in UTC.


```python
@property
def last_saved_time(self) -> datetime.datetime:
    ...

@last_saved_time.setter
def last_saved_time(self, value: datetime.datetime):
    ...

```

### Remarks

For documents originated from RTF format this property returns the local time of last save operation.

Aspose.Words does not update this property.




### Examples

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(file_name=MY_DIR + 'Document.docx')
builder = aw.DocumentBuilder(doc=doc)
builder.move_to_document_end()
builder.writeln(' Date this document was last saved:')
# Podemos usar el campo SAVEDATE para mostrar la fecha y hora de la última operación de guardado en el documento.
# La operación de guardado a la que se refieren estos campos es el guardado manual en una aplicación como Microsoft Word,
# no el método Save del documento.
# A continuación se presentan tres tipos de calendario diferentes según los cuales el campo SAVEDATE puede mostrar la fecha/hora.
# 1 -  Calendario lunar islámico:
builder.write('According to the Lunar Calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_lunar_calendar = True
self.assertEqual(' SAVEDATE  \\h', field.get_field_code())
# 2 -  Calendario Umm al-Qura:
builder.write('\nAccording to the Umm al-Qura calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_um_al_qura_calendar = True
self.assertEqual(' SAVEDATE  \\u', field.get_field_code())
# 3 -  Calendario Nacional Indio:
builder.write('\nAccording to the Indian National calendar - ')
field = builder.insert_field(field_type=FieldType.FIELD_SAVE_DATE, update_field=True).as_field_save_date()
field.use_saka_era_calendar = True
self.assertEqual(' SAVEDATE  \\s', field.get_field_code())
# Los campos SAVEDATE obtienen sus valores de fecha/hora de la propiedad incorporada LastSavedTime.
# El método Save del documento no actualizará este valor, pero aún podemos actualizarlo manualmente.
doc.built_in_document_properties.last_saved_time = datetime.datetime.now()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.SAVEDATE.docx')
```

### See Also

* module [aspose.words.properties](../../)
* class [BuiltInDocumentProperties](../)

