﻿---
title: FieldDatabase class
second_title: Aspose.Words for Python via .NET API Reference
description: "Implements the DATABASE field"
type: docs
weight: 280
url: /python-net/aspose.words.fields/fielddatabase/
---

## FieldDatabase class

Implements the DATABASE field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




Inserts the results of a database query into a WordprocessingML table.


**Inheritance:** [FieldDatabase](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldDatabase()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [connection](./connection/) | Gets or sets a connection to the data. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [file_name](./file_name/) | Gets or sets the complete path and file name of the database |
| [first_record](./first_record/) | Gets or sets the integral record number of the first data record to insert. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [format_attributes](./format_attributes/) | Gets or sets which attributes of the format are to be applied to the table. |
| [insert_headings](./insert_headings/) | Gets or sets whether to insert the field names from the database as column headings in the resulting table. |
| [insert_once_on_mail_merge](./insert_once_on_mail_merge/) | Gets or sets whether to insert data at the beginning of a merge. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [last_record](./last_record/) | Gets or sets the integral record number of the last data record to insert. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [query](./query/) | Gets or sets a set of SQL instructions that query the database. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [table_format](./table_format/) | Gets or sets the format that is to be applied to the result of the database query. |
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

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

