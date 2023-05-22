﻿---
title: FieldQuote class
linktitle: FieldQuote class
articleTitle: FieldQuote class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldQuote class. Implements the QUOTE field"
type: docs
weight: 850
url: /python-net/aspose.words.fields/fieldquote/
---

## FieldQuote class

Implements the QUOTE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the specified text.


**Inheritance:** [FieldQuote](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldQuote()](./__init__/#default) | The default constructor. |

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

Shows to use the QUOTE field.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# Insert a QUOTE field, which will display the value of its Text property.
field = builder.insert_field(aw.fields.FieldType.FIELD_QUOTE, True).as_field_quote()
field.text = "\"Quoted text\""

self.assertEqual(" QUOTE  \"\\\"Quoted text\\\"\"", field.get_field_code())

# Insert a QUOTE field and nest a DATE field inside it.
# DATE fields update their value to the current date every time we open the document using Microsoft Word.
# Nesting the DATE field inside the QUOTE field like this will freeze its value
# to the date when we created the document.
builder.write("\nDocument creation date: ")
field = builder.insert_field(aw.fields.FieldType.FIELD_QUOTE, True).as_field_quote()
builder.move_to(field.separator)
builder.insert_field(aw.fields.FieldType.FIELD_DATE, True)

today = datetime.now().strftime("%d/%m/%Y").lstrip('0')

self.assertEqual(" QUOTE \u0013 DATE \u0014" + today + "\u0015", field.get_field_code())

# Update all the fields to display their correct results.
doc.update_fields()

self.assertEqual("\"Quoted text\"", doc.range.fields[0].result)

doc.save(ARTIFACTS_DIR + "Field.field_quote.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

