---
title: FieldShape.text property
linktitle: text property
articleTitle: text property
second_title: Aspose.Words for Python
description: "FieldShape.text property. Gets or sets the text to retrieve."
type: docs
weight: 20
url: /es/python-net/aspose.words.fields/fieldshape/text/
---

## FieldShape.text property

Gets or sets the text to retrieve.


```python
@property
def text(self) -> str:
    ...

@text.setter
def text(self, value: str):
    ...

```

### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# El campo BIDIOUTLINE numera los párrafos como los campos AUTONUM/LISTNUM,
# pero solo es visible cuando se habilita un idioma de edición de derecha a izquierda, como el hebreo o el árabe.
# El siguiente campo mostrará ".1", el equivalente RTL del número de lista "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Agregue dos campos BIDIOUTLINE más, que mostrarán ".2" y ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Establezca la alineación horizontal del texto para cada párrafo del documento en RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Si habilitamos un idioma de edición de derecha a izquierda en Microsoft Word, nuestros campos mostrarán números.
# De lo contrario, mostrarán "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Abra un documento que fue creado en Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Si abrimos el documento de Word y pulsamos Alt+F9, veremos un campo SHAPE y un campo EMBED.
# Un campo SHAPE es el ancla/lienzo para un objeto AutoShape con el estilo de ajuste "In line with text" habilitado.
# Un campo EMBED tiene la misma función, pero para un objeto incrustado,
# como una hoja de cálculo de un documento Excel externo.
# Sin embargo, estos campos no aparecerán en la colección Fields del documento.
self.assertEqual(0, doc.range.fields.count)
# Estos campos solo son compatibles con versiones antiguas de Microsoft Word.
# El proceso de carga del documento convertirá estos campos en objetos Shape,
# que podemos acceder en la colección de nodos del documento.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# El primer nodo Shape corresponde al campo SHAPE en el documento de entrada,
# que es el lienzo en línea para el AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# El segundo nodo Shape es el propio AutoShape.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# El tercer Shape es lo que era el campo EMBED que contenía la hoja de cálculo externa.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../../)
* class [FieldShape](../)

