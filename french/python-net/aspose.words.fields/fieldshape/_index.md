---
title: FieldShape class
linktitle: FieldShape class
articleTitle: FieldShape class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldShape class. Implements the SHAPE field"
type: docs
weight: 950
url: /fr/python-net/aspose.words.fields/fieldshape/
---

## FieldShape class

Implements the SHAPE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Retrieves the specified text.


**Inheritance:** [FieldShape](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldShape()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [text](./text/) | Gets or sets the text to retrieve. |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |

### Methods

| Name | Description |
| --- | --- |
|[ get_field_code()](../field/get_field_code/#default) | Returns text between field start and field separator (or field end if there is no separator). Both field code and field result of child fields are included.<br>(Inherited from [Field](../field/)) |
|[ get_field_code(include_child_field_codes)](../field/get_field_code/#bool) | Returns text between field start and field separator (or field end if there is no separator).<br>(Inherited from [Field](../field/)) |
|[ remove()](../field/remove/#default) | Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns ``None``.<br>(Inherited from [Field](../field/)) |
|[ unlink()](../field/unlink/#default) | Performs the field unlink.<br>(Inherited from [Field](../field/)) |
|[ update()](../field/update/#default) | Performs the field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |
|[ update(ignore_merge_format)](../field/update/#bool) | Performs a field update. Throws if the field is being updated already.<br>(Inherited from [Field](../field/)) |

### Examples

Shows how to create right-to-left language-compatible lists with BIDIOUTLINE fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Le champ BIDIOUTLINE numérote les paragraphes comme les champs AUTONUM/LISTNUM,
# mais n'est visible que lorsqu'une langue d'édition de droite à gauche est activée, comme l'hébreu ou l'arabe.
# Le champ suivant affichera ".1", l'équivalent RTL du numéro de liste "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Ajoutez deux champs BIDIOUTLINE supplémentaires, qui afficheront ".2" et ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Définissez l'alignement horizontal du texte pour chaque paragraphe du document sur RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Si nous activons une langue d'édition de droite à gauche dans Microsoft Word, nos champs afficheront des nombres.
# Sinon, ils afficheront "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Ouvrez un document qui a été créé dans Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Si nous ouvrons le document Word et appuyons sur Alt+F9, nous verrons un champ SHAPE et un champ EMBED.
# Un champ SHAPE est l'ancre/zone de dessin pour un objet AutoShape avec le style de retour à la ligne « En ligne avec le texte » activé.
# Un champ EMBED a la même fonction, mais pour un objet incorporé,
# comme une feuille de calcul provenant d'un document Excel externe.
# Cependant, ces champs n'apparaîtront pas dans la collection Fields du document.
self.assertEqual(0, doc.range.fields.count)
# Ces champs ne sont pris en charge que par les anciennes versions de Microsoft Word.
# Le processus de chargement du document convertira ces champs en objets Shape,
# que nous pouvons accéder dans la collection de nœuds du document.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# Le premier nœud Shape correspond au champ SHAPE dans le document d'entrée,
# qui est la zone de dessin en ligne pour l'AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# Le deuxième nœud Shape est l'AutoShape elle-même.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Le troisième Shape était le champ EMBED qui contenait la feuille de calcul externe.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

