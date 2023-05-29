﻿---
title: FieldSaveDate class
linktitle: FieldSaveDate class
articleTitle: FieldSaveDate class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldSaveDate class. Implements the SAVEDATE field"
type: docs
weight: 890
url: /python-net/aspose.words.fields/fieldsavedate/
---

## FieldSaveDate class

Implements the SAVEDATE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the date and time on which the document was last saved. By default, the Gregorian calendar is used.


**Inheritance:** [FieldSaveDate](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldSaveDate()](./__init__/#default) | The default constructor. |

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
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_lunar_calendar](./use_lunar_calendar/) | Gets or sets whether to use the Hijri Lunar or Hebrew Lunar calendar. |
| [use_saka_era_calendar](./use_saka_era_calendar/) | Gets or sets whether to use the Saka Era calendar. |
| [use_um_al_qura_calendar](./use_um_al_qura_calendar/) | Gets or sets whether to use the Um-al-Qura calendar. |

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

Shows how to use the SAVEDATE field to display the date/time of the document's most recent save operation performed using Microsoft Word.

```python
doc = aw.Document(MY_DIR + "Document.docx")
builder = aw.DocumentBuilder(doc)
builder.move_to_document_end()
builder.writeln(" Date this document was last saved:")

# We can use the SAVEDATE field to display the last save operation's date and time on the document.
# The save operation that these fields refer to is the manual save in an application like Microsoft Word,
# not the document's "save" method.
# Below are three different calendar types according to which the SAVEDATE field can display the date/time.
# 1 -  Islamic Lunar Calendar:
builder.write("According to the Lunar Calendar - ")
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_lunar_calendar = True

self.assertEqual(" SAVEDATE  \\h", field.get_field_code())

# 2 -  Umm al-Qura calendar:
builder.write("\nAccording to the Umm al-Qura calendar - ")
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_um_al_qura_calendar = True

self.assertEqual(" SAVEDATE  \\u", field.get_field_code())

# 3 -  Indian National calendar:
builder.write("\nAccording to the Indian National calendar - ")
field = builder.insert_field(aw.fields.FieldType.FIELD_SAVE_DATE, True).as_field_save_date()
field.use_saka_era_calendar = True

self.assertEqual(" SAVEDATE  \\s", field.get_field_code())

# The SAVEDATE fields draw their date/time values from the "last_saved_time" built-in property.
# The document's Save method will not update this value, but we can still update it manually.
doc.built_in_document_properties.last_saved_time = datetime.now()

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_save_date.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

