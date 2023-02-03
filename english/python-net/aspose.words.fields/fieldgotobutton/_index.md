---
title: FieldGoToButton class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the GOTOBUTTON field"
type: docs
weight: 510
url: /python-net/aspose.words.fields/fieldgotobutton/
---

## FieldGoToButton class

Implements the GOTOBUTTON field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts a jump command, such that when it is activated, the insertion point of the document is
moved to the specified location.


**Inheritance:** [FieldGoToButton](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldGoToButton()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [display_text](./display_text/) | Gets or sets the text of the "button" that appears in the document, such that it can be selected to activate the jump. |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [location](./location/) | Gets or sets the name of a bookmark, a page number, or some other item to jump to. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
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

Shows to insert a GOTOBUTTON field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Add a GOTOBUTTON field. When we double-click this field in Microsoft Word,
# it will take the text cursor to the bookmark whose name the Location property references.
field = builder.insert_field(aw.fields.FieldType.FIELD_GO_TO_BUTTON, True).as_field_go_to_button()
field.display_text = "My Button"
field.location = "MyBookmark"

self.assertEqual(" GOTOBUTTON  MyBookmark My Button", field.get_field_code())

# Insert a valid bookmark for the field to reference.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark(field.location)
builder.writeln("Bookmark text contents.")
builder.end_bookmark(field.location)

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_go_to_button.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

