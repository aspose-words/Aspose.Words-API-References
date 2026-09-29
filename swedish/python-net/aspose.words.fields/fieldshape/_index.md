---
title: FieldShape class
linktitle: FieldShape class
articleTitle: FieldShape class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldShape class. Implements the SHAPE field"
type: docs
weight: 950
url: /sv/python-net/aspose.words.fields/fieldshape/
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
# BIDIOUTLINE-fältet numrerar stycken som AUTONUM/LISTNUM-fälten,
# men är endast synligt när ett höger-till-vänster redigeringsspråk är aktiverat, såsom hebreiska eller arabiska.
# Följande fält kommer att visa ".1", den RTL-ekvivalenten till listnumret "1.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True).as_field_bidi_outline()
builder.writeln('שלום')
self.assertEqual(' BIDIOUTLINE ', field.get_field_code())
# Lägg till två ytterligare BIDIOUTLINE-fält, som kommer att visa ".2" och ".3".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
builder.insert_field(field_type=aw.fields.FieldType.FIELD_BIDI_OUTLINE, update_field=True)
builder.writeln('שלום')
# Ställ in horisontell textjustering för varje stycke i dokumentet till RTL.
for para in doc.get_child_nodes(aw.NodeType.PARAGRAPH, True):
    para = para.as_paragraph()
    para.paragraph_format.bidi = True
# Om vi aktiverar ett höger-till-vänster redigeringsspråk i Microsoft Word kommer våra fält att visa siffror.
# Annars kommer de att visa "###".
doc.save(file_name=ARTIFACTS_DIR + 'Field.BIDIOUTLINE.docx')
```

Shows how some older Microsoft Word fields such as SHAPE and EMBED are handled during loading.

```python
# Öppna ett dokument som skapades i Microsoft Word 2003.
doc = aw.Document(file_name=MY_DIR + 'Legacy fields.doc')
# Om vi öppnar Word-dokumentet och trycker på Alt+F9, kommer vi att se ett SHAPE- och ett EMBED-fält.
# Ett SHAPE-fält är ankaret/ytan för ett AutoShape-objekt med omslagstilen "In line with text" aktiverad.
# Ett EMBED-fält har samma funktion, men för ett inbäddat objekt,
# till exempel ett kalkylblad från ett externt Excel-dokument.
# Dessa fält kommer dock inte att visas i dokumentets Fields-samling.
self.assertEqual(0, doc.range.fields.count)
# Dessa fält stöds endast av äldre versioner av Microsoft Word.
# Dokumentläsningsprocessen kommer att konvertera dessa fält till Shape-objekt,
# som vi kan komma åt i dokumentets node-samling.
shapes = doc.get_child_nodes(aw.NodeType.SHAPE, True)
self.assertEqual(3, shapes.count)
# Den första Shape-noden motsvarar SHAPE-fältet i indatadokumentet,
# som är den inbäddade ytan för AutoShape.
shape = shapes[0].as_shape()
self.assertEqual(aw.drawing.ShapeType.IMAGE, shape.shape_type)
# Den andra Shape-noden är själva AutoShape.
shape = shapes[1].as_shape()
self.assertEqual(aw.drawing.ShapeType.CAN, shape.shape_type)
# Den tredje Shape är det som var EMBED-fältet som innehöll det externa kalkylbladet.
shape = shapes[2].as_shape()
self.assertEqual(aw.drawing.ShapeType.OLE_OBJECT, shape.shape_type)
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

