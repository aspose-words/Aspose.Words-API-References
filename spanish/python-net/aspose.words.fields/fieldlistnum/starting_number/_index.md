---
title: FieldListNum.starting_number property
linktitle: starting_number property
articleTitle: starting_number property
second_title: Aspose.Words for Python
description: "FieldListNum.starting_number property. Gets or sets the starting value for this field."
type: docs
weight: 50
url: /es/python-net/aspose.words.fields/fieldlistnum/starting_number/
---

## FieldListNum.starting_number property

Gets or sets the starting value for this field.


```python
@property
def starting_number(self) -> str:
    ...

@starting_number.setter
def starting_number(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Los campos LISTNUM muestran un número que se incrementa en cada campo LISTNUM.
# Estos campos también tienen una variedad de opciones que nos permiten usarlos para emular listas numeradas.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Las listas comienzan a contar en 1 por defecto, pero podemos establecer este número a un valor diferente, como 0.
# Este campo mostrará "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# Los campos LISTNUM mantienen recuentos separados para cada nivel de lista.
# Insertar un campo LISTNUM en el mismo párrafo que otro campo LISTNUM
# incrementa el nivel de la lista en lugar del recuento.
# El siguiente campo continuará el recuento que iniciamos arriba y mostrará un valor de "1" en el nivel de lista 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Este campo iniciará un recuento en el nivel de lista 2. Mostrará un valor de "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Este campo iniciará un recuento en el nivel de lista 3. Mostrará un valor de "1".
# Los diferentes niveles de lista tienen un formato diferente,
# por lo que estos campos combinados mostrarán un valor de "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# El siguiente campo LISTNUM que insertamos continuará el recuento en el nivel de lista
# en el que estaba el campo LISTNUM anterior.
# Podemos usar la propiedad "ListLevel" para saltar a un nivel de lista diferente.
# Si este campo LISTNUM permaneciera en el nivel de lista 3, mostraría "ii)",
# pero, como lo hemos movido al nivel de lista 2, continúa el recuento en ese nivel y muestra "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Podemos establecer la propiedad ListName para que el campo emule un tipo de campo AUTONUM diferente.
# "NumberDefault" emula AUTONUM, "OutlineDefault" emula AUTONUMOUT,
# y "LegalDefault" emula campos AUTONUMLGL.
# El nombre de lista "OutlineDefault" con 1 como número inicial resultará en mostrar "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# El ListName no se mantiene del campo anterior, por lo que necesitaremos establecerlo para cada campo nuevo.
# Este campo continúa el recuento con el nombre de lista diferente y muestra "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldListNum](../)

