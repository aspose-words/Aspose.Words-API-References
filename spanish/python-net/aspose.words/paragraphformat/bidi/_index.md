---
title: ParagraphFormat.bidi property
linktitle: bidi property
articleTitle: bidi property
second_title: Aspose.Words for Python
description: "ParagraphFormat.bidi property. Gets or sets whether this is a right-to-left paragraph."
type: docs
weight: 50
url: /es/python-net/aspose.words/paragraphformat/bidi/
---

## ParagraphFormat.bidi property

Gets or sets whether this is a right-to-left paragraph.


```python
@property
def bidi(self) -> bool:
    ...

@bidi.setter
def bidi(self, value: bool):
    ...

```

### Remarks

When ``True``, the runs and other inline objects in this paragraph
are laid out right to left.




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

Shows how to detect plaintext document text direction.

```python
# Cree un objeto "TxtLoadOptions", que podemos pasar al constructor de un documento
# para modificar cómo cargamos un documento de texto sin formato.
load_options = aw.loading.TxtLoadOptions()
# Establezca la propiedad "DocumentDirection" a "DocumentDirection.Auto" para que detecte automáticamente
# la dirección de cada párrafo de texto que Aspose.Words carga desde texto sin formato.
# La propiedad "Bidi" de cada párrafo almacenará su dirección.
load_options.document_direction = aw.loading.DocumentDirection.AUTO
# Detecte texto hebreo como de derecha a izquierda.
doc = aw.Document(file_name=MY_DIR + 'Hebrew text.txt', load_options=load_options)
self.assertTrue(doc.first_section.body.first_paragraph.paragraph_format.bidi)
# Detecte texto inglés como de derecha a izquierda.
doc = aw.Document(file_name=MY_DIR + 'English text.txt', load_options=load_options)
self.assertFalse(doc.first_section.body.first_paragraph.paragraph_format.bidi)
```

### See Also

* module [aspose.words](../../)
* class [ParagraphFormat](../)

