---
title: FieldAutoNum.separator_character property
linktitle: separator_character property
articleTitle: separator_character property
second_title: Aspose.Words for Python
description: "FieldAutoNum.separator_character property. Gets or sets the separator character to be used."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldautonum/separator_character/
---

## FieldAutoNum.separator_character property

Gets or sets the separator character to be used.


```python
@property
def separator_character(self) -> str:
    ...

@separator_character.setter
def separator_character(self, value: str):
    ...

```

### Examples

Shows how to number paragraphs using autonum fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Cada campo AUTONUM muestra el valor actual de un recuento continuo de campos AUTONUM,
# permitiéndonos numerar automáticamente los elementos como una lista numerada.
# Este campo mostrará un número "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 1.')
self.assertEqual(' AUTONUM ', field.get_field_code())
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_AUTO_NUM, update_field=True).as_field_auto_num()
builder.writeln('\tParagraph 2.')
# El carácter separador, que aparece en el resultado del campo inmediatamente después del número, es un punto por defecto.
# Si dejamos esta propiedad nula, nuestro segundo campo AUTONUM mostrará "2." en el documento.
self.assertIsNone(field.separator_character)
# Podemos establecer esta propiedad para aplicar el primer carácter de su cadena como el nuevo carácter separador.
# En este caso, nuestro campo AUTONUM ahora mostrará "2:".
field.separator_character = ':'
self.assertEqual(' AUTONUM  \\s :', field.get_field_code())
doc.save(file_name=ARTIFACTS_DIR + 'Field.AUTONUM.docx')
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldAutoNum](../)

