---
title: FieldTA class
linktitle: FieldTA class
articleTitle: FieldTA class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldTA class. Implements the TA field"
type: docs
weight: 1010
url: /ru/python-net/aspose.words.fields/fieldta/
---

## FieldTA class

Implements the TA field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Defines the text and page number for a table of authorities entry, which is used by a TOA field.


**Inheritance:** [FieldTA](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldTA()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_category](./entry_category/) | Gets or sets the integral entry category, which is a number that corresponds to the order of categories. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [is_bold](./is_bold/) | Gets or sets whether to apply bold formatting to the page number for the entry. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_italic](./is_italic/) | Gets or sets whether to apply italic formatting to the page number for the entry. |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [long_citation](./long_citation/) | Gets or sets the long citation for the entry. |
| [page_range_bookmark_name](./page_range_bookmark_name/) | Gets or sets the name of the bookmark that marks a range of pages that is inserted as the entry's page number. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [short_citation](./short_citation/) | Gets or sets the short citation for the entry. |
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

Shows how to build and customize a table of authorities using TOA and TA fields.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Вставьте поле TOA, которое создаст запись для каждого поля TA в документе,
# отображая длинные ссылки и номера страниц для каждой записи.
field_toa = builder.insert_field(field_type=FieldType.FIELD_TOA, update_field=False).as_field_toa()
# Установите категорию записи для нашей таблицы. Этот TOA теперь будет включать только поля TA
# которые имеют соответствующее значение в их свойстве EntryCategory.
field_toa.entry_category = '1'
# Более того, категория Таблицы Авторитетов с индексом 1 — "Cases",
# которая будет отображаться как заголовок нашей таблицы, если установить эту переменную в true.
field_toa.use_heading = True
# Мы можем дополнительно фильтровать поля TA, задав закладку, в пределах которой они должны находиться в границах TOA.
field_toa.bookmark_name = 'MyBookmark'
# По умолчанию между цитатой поля TA появляется пунктирная табуляция на всю ширину страницы
# и её номером страницы. Мы можем заменить её любым текстом, который задаём в этом свойстве.
# Вставка символа табуляции сохранит оригинальную табуляцию.
field_toa.entry_separator = ' \t p.'
# Если у нас есть несколько записей TA, которые используют одну и ту же длинную цитату,
# все их соответствующие номера страниц отобразятся в одной строке.
# Мы можем использовать это свойство, чтобы указать строку, которая будет разделять их номера страниц.
field_toa.page_number_list_separator = ' & p. '
# Мы можем установить это значение в true, чтобы наша таблица отображала слово "passim"
# если в одной строке пять или более номеров страниц.
field_toa.use_passim = True
# Одно поле TA может ссылаться на диапазон страниц.
# Мы можем указать здесь строку, которая будет отображаться между начальным и конечным номерами страниц для таких диапазонов.
field_toa.page_range_separator = ' to '
# Формат из полей TA будет перенесён в нашу таблицу.
# Мы можем отключить это, установив флаг RemoveEntryFormatting.
field_toa.remove_entry_formatting = True
builder.font.color = Color.green
builder.font.name = 'Arial Black'
self.assertEqual(' TOA  \\c 1 \\h \\b MyBookmark \\e " \t p." \\l " & p. " \\p \\g " to " \\f', field_toa.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
# Это поле TA не появится как запись в TOA, поскольку оно находится за пределами
# границами закладки, которые задаёт свойство BookmarkName у TOA.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 1')
self.assertEqual(' TA  \\c 1 \\l "Source 1"', field_ta.get_field_code())
# Это поле TA находится внутри закладки,
# но категория записи не совпадает с таблицей, поэтому поле TA не будет её включать.
builder.start_bookmark('MyBookmark')
field_ta = ExField._insert_toa_entry(builder, '2', 'Source 2')
# Эта запись появится в таблице.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
# Таблица TOA не отображает короткие цитаты,
# но мы можем использовать их как сокращение для обращения к громоздким названиям источников, на которые ссылаются несколько полей TA.
field_ta.short_citation = 'S.3'
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\s S.3', field_ta.get_field_code())
# Мы можем отформатировать номер страницы, сделав его полужирным/курсивным, используя следующие свойства.
# Мы всё равно увидим эти эффекты, если установим нашу таблицу игнорировать форматирование.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 2')
field_ta.is_bold = True
field_ta.is_italic = True
self.assertEqual(' TA  \\c 1 \\l "Source 2" \\b \\i', field_ta.get_field_code())
# Мы можем настроить поля TA так, чтобы их записи TOA ссылались на диапазон страниц, охватываемый закладкой.
# Обратите внимание, что эта запись ссылается на тот же источник, что и выше, чтобы поделиться одной строкой в нашей таблице.
# Эта строка будет содержать номер страницы записи выше и диапазон страниц этой записи,
# с разделителями списка страниц и диапазона номеров страниц таблицы между номерами страниц.
field_ta = ExField._insert_toa_entry(builder, '1', 'Source 3')
field_ta.page_range_bookmark_name = 'MyMultiPageBookmark'
builder.start_bookmark('MyMultiPageBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.end_bookmark('MyMultiPageBookmark')
self.assertEqual(' TA  \\c 1 \\l "Source 3" \\r MyMultiPageBookmark', field_ta.get_field_code())
# Если мы включили функцию "Passim" в нашей таблице, наличие 5 или более записей TA с одинаковым источником активирует её.
i = 0
while i < 5:
    ExField._insert_toa_entry(builder, '1', 'Source 4')
    i += 1
builder.end_bookmark('MyBookmark')
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.TOA.TA.docx')
```

Shows how to build and customize a table of authorities using TOA and TA fields (InsertToaEntry).

```python
@staticmethod
def _insert_toa_entry(builder, entry_category, long_citation):
    field = builder.insert_field(field_type=aw.fields.FieldType.FIELD_TOA_ENTRY, update_field=False).as_field_ta()
    field.entry_category = entry_category
    field.long_citation = long_citation
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    return field
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

