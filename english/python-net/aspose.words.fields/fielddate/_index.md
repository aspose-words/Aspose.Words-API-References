---
title: FieldDate class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the DATE field"
type: docs
weight: 310
url: /python-net/aspose.words.fields/fielddate/
---

## FieldDate class

Implements the DATE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts the current date and time. By default, the Gregorian calendar is used.


**Inheritance:** [FieldDate](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldDate()](./__init__/#default) | The default constructor. |

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
| [use_last_format](./use_last_format/) | Gets or sets whether to use a format last used by the hosting application when inserting a new DATE field. |
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

Shows how to use DATE fields to display dates according to different kinds of calendars.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

# If we want the text in the document always to display the correct date, we can use a DATE field.
# Below are three types of cultural calendars that a DATE field can use to display a date.
# 1 -  Islamic Lunar Calendar:
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_lunar_calendar = True
self.assertEqual(" DATE  \\h", field.get_field_code())
builder.writeln()

# 2 -  Umm al-Qura calendar:
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_um_al_qura_calendar = True
self.assertEqual(" DATE  \\u", field.get_field_code())
builder.writeln()

# 3 -  Indian National Calendar:
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_saka_era_calendar = True
self.assertEqual(" DATE  \\s", field.get_field_code())
builder.writeln()

# Insert a DATE field and set its calendar type to the one last used by the host application.
# In Microsoft Word, the type will be the most recently used in the Insert -> Text -> Date and Time dialog box.
field = builder.insert_field(aw.fields.FieldType.FIELD_DATE, True).as_field_date()
field.use_last_format = True
self.assertEqual(" DATE  \\l", field.get_field_code())
builder.writeln()

doc.update_fields()
doc.save(ARTIFACTS_DIR + "Field.field_date.docx")
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

