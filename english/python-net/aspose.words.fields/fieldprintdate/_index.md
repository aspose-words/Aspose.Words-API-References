---
title: FieldPrintDate class
linktitle: FieldPrintDate class
articleTitle: FieldPrintDate class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldPrintDate class. Implements the PRINTDATE field"
type: docs
weight: 830
url: /python-net/aspose.words.fields/fieldprintdate/
---

## FieldPrintDate class

Implements the PRINTDATE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Retrieves the date and time on which the document was last printed. By default, the Gregorian calendar is used.


**Inheritance:** [FieldPrintDate](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldPrintDate()](./__init__/#default) | The default constructor. |

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

Shows read PRINTDATE fields.

```python
doc = aw.Document(MY_DIR + "Field sample - PRINTDATE.docx")

# When a document is printed by a printer or printed as a PDF (but not exported to PDF),
# PRINTDATE fields will display the print operation's date/time.
# If no printing has taken place, these fields will display "0/0/0000".
field = doc.range.fields[0].as_field_print_date()

self.assertEqual("3/25/2020 12:00:00 AM", field.result)
self.assertEqual(" PRINTDATE ", field.get_field_code())

# Below are three different calendar types according to which the PRINTDATE field
# can display the date and time of the last printing operation.
# 1 -  Islamic Lunar Calendar:
field = doc.range.fields[1].as_field_print_date()

self.assertTrue(field.use_lunar_calendar)
self.assertEqual("8/1/1441 12:00:00 AM", field.result)
self.assertEqual(" PRINTDATE  \\h", field.get_field_code())

field = doc.range.fields[2].as_field_print_date()

# 2 -  Umm al-Qura calendar:
self.assertTrue(field.use_um_al_qura_calendar)
self.assertEqual("8/1/1441 12:00:00 AM", field.result)
self.assertEqual(" PRINTDATE  \\u", field.get_field_code())

field = doc.range.fields[3].as_field_print_date()

# 3 -  Indian National Calendar:
self.assertTrue(field.use_saka_era_calendar)
self.assertEqual("1/5/1942 12:00:00 AM", field.result)
self.assertEqual(" PRINTDATE  \\s", field.get_field_code())
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

