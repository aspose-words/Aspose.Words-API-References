---
title: FieldListNum class
linktitle: FieldListNum class
articleTitle: FieldListNum class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldListNum class. Implements the LISTNUM field"
type: docs
weight: 660
url: /ru/python-net/aspose.words.fields/fieldlistnum/
---

## FieldListNum class

Implements the LISTNUM field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




**Inheritance:** [FieldListNum](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldListNum()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [has_list_name](./has_list_name/) | Returns a value indicating whether the name of an abstract numbering definition is provided by the field's code. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [list_level](./list_level/) | Gets or sets the level in the list, overriding the default behavior of the field. |
| [list_name](./list_name/) | Gets or sets the name of the abstract numbering definition used for the numbering. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [starting_number](./starting_number/) | Gets or sets the starting value for this field. |
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

Shows how to number paragraphs with LISTNUM fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Поля LISTNUM отображают число, которое увеличивается в каждом поле LISTNUM.
# Эти поля также имеют разнообразные параметры, позволяющие использовать их для имитации нумерованных списков.
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
# Списки по умолчанию начинают счет с 1, но мы можем установить другое значение, например 0.
# Это поле отобразит "0)".
field.starting_number = '0'
builder.writeln('Paragraph 1')
self.assertEqual(' LISTNUM  \\s 0', field.get_field_code())
# Поля LISTNUM поддерживают отдельные счетчики для каждого уровня списка.
# Вставка поля LISTNUM в тот же абзац, что и другое поле LISTNUM
# увеличивает уровень списка вместо счетчика.
# Следующее поле продолжит счет, который мы начали выше, и отобразит значение "1" на уровне списка 1.
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Это поле начнет счет на уровне списка 2. Оно отобразит значение "1".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
# Это поле начнет счет на уровне списка 3. Оно отобразит значение "1".
# Разные уровни списка имеют разное форматирование,
# поэтому эти поля вместе отобразят значение "1)a)i)".
builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True)
builder.writeln('Paragraph 2')
# Следующее поле LISTNUM, которое мы вставим, продолжит счёт на уровне списка
# на котором находилось предыдущее поле LISTNUM.
# Мы можем использовать свойство "ListLevel", чтобы перейти к другому уровню списка.
# Если бы это поле LISTNUM оставалось на уровне списка 3, оно отобразило бы "ii)",
# но, поскольку мы переместили его на уровень списка 2, оно продолжает счёт на этом уровне и отображает "b)".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_level = '2'
builder.writeln('Paragraph 3')
self.assertEqual(' LISTNUM  \\l 2', field.get_field_code())
# Мы можем установить свойство ListName, чтобы поле имитировало другой тип поля AUTONUM.
# "NumberDefault" имитирует AUTONUM, "OutlineDefault" имитирует AUTONUMOUT,
# а "LegalDefault" имитирует поля AUTONUMLGL.
# Имя списка "OutlineDefault" с 1 в качестве начального номера приведёт к отображению "I.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.starting_number = '1'
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 4')
self.assertTrue(field.has_list_name)
self.assertEqual(' LISTNUM  OutlineDefault \\s 1', field.get_field_code())
# ListName не переносится от предыдущего поля, поэтому нам придётся задавать его для каждого нового поля.
# Это поле продолжает счёт с другим именем списка и отображает "II.".
field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_LIST_NUM, update_field=True).as_field_list_num()
field.list_name = 'OutlineDefault'
builder.writeln('Paragraph 5')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.LISTNUM.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

