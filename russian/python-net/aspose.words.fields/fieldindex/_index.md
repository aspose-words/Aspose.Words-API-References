---
title: FieldIndex class
linktitle: FieldIndex class
articleTitle: FieldIndex class
second_title: Aspose.Words for Python
description: "aspose.words.fields.FieldIndex class. Implements the INDEX field"
type: docs
weight: 600
url: /ru/python-net/aspose.words.fields/fieldindex/
---

## FieldIndex class

Implements the INDEX field.
To learn more, visit the [Working with Fields](https://docs.aspose.com/words/python-net/working-with-fields/) documentation article.




### Remarks

Builds an index using the index entries specified by XE fields, and inserts that index at this place in the document.


**Inheritance:** [FieldIndex](./) → [Field](../field/)

### Constructors
| Name | Description |
| --- | --- |
| [FieldIndex()](./__init__/#default) | The default constructor. |

### Properties

| Name | Description |
| --- | --- |
| [bookmark_name](./bookmark_name/) | Gets or sets the name of the bookmark that marks the portion of the document used to build the index. |
| [cross_reference_separator](./cross_reference_separator/) | Gets or sets the character sequence that is used to separate cross references and other entries. |
| [display_result](../field/display_result/) | Gets the text that represents the displayed field result.<br>(Inherited from [Field](../field/)) |
| [end](../field/end/) | Gets the node that represents the field end.<br>(Inherited from [Field](../field/)) |
| [entry_type](./entry_type/) | Gets or sets an index entry type used to build the index. |
| [format](../field/format/) | Gets a [FieldFormat](../fieldformat/) object that provides typed access to field's formatting.<br>(Inherited from [Field](../field/)) |
| [has_page_number_separator](./has_page_number_separator/) | Gets a value indicating whether a page number separator is overridden through the field's code. |
| [has_sequence_name](./has_sequence_name/) | Gets a value indicating whether a sequence should be used while the field's result building. |
| [heading](./heading/) | Gets or sets a heading that appears at the start of each set of entries for any given letter. |
| [is_dirty](../field/is_dirty/) | Gets or sets whether the current result of the field is no longer correct (stale) due to other modifications made to the document.<br>(Inherited from [Field](../field/)) |
| [is_locked](../field/is_locked/) | Gets or sets whether the field is locked (should not recalculate its result).<br>(Inherited from [Field](../field/)) |
| [language_id](./language_id/) | Gets or sets the language ID used to generate the index. |
| [letter_range](./letter_range/) | Gets or sets a range of letters to which limit the index. |
| [locale_id](../field/locale_id/) | Gets or sets the LCID of the field.<br>(Inherited from [Field](../field/)) |
| [number_of_columns](./number_of_columns/) | Gets or sets the number of columns per page used when building the index. |
| [page_number_list_separator](./page_number_list_separator/) | Gets or sets the character sequence that is used to separate two page numbers in a page number list. |
| [page_number_separator](./page_number_separator/) | Gets or sets the character sequence that is used to separate an index entry and its page number. |
| [page_range_separator](./page_range_separator/) | Gets or sets the character sequence that is used to separate the start and end of a page range. |
| [result](../field/result/) | Gets or sets text that is between the field separator and field end.<br>(Inherited from [Field](../field/)) |
| [run_subentries_on_same_line](./run_subentries_on_same_line/) | Gets or sets whether run subentries into the same line as the main entry. |
| [separator](../field/separator/) | Gets the node that represents the field separator. Can be ``None``.<br>(Inherited from [Field](../field/)) |
| [sequence_name](./sequence_name/) | Gets or sets the name of a sequence whose number is included with the page number. |
| [sequence_separator](./sequence_separator/) | Gets or sets the character sequence that is used to separate sequence numbers and page numbers. |
| [start](../field/start/) | Gets the node that represents the start of the field.<br>(Inherited from [Field](../field/)) |
| [type](../field/type/) | Gets the Microsoft Word field type.<br>(Inherited from [Field](../field/)) |
| [use_yomi](./use_yomi/) | Gets or sets whether to enable the use of yomi text for index entries. |

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

Shows how to create an INDEX field, and then use XE fields to populate it with entries.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет показывать значение свойства Text поля XE слева
# и страницу, содержащую поле XE, справа.
# Если у полей XE одинаковое значение в их свойстве "Text",
# поле INDEX сгруппирует их в одну запись.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
# Настройте поле INDEX так, чтобы оно отображало только поля XE, находящиеся в пределах
# закладки с именем "MainBookmark" и у которых свойства "EntryType" имеют значение "A".
# Для полей INDEX и XE свойство "EntryType" использует только первый символ строкового значения.
index.bookmark_name = 'MainBookmark'
index.entry_type = 'A'
self.assertEqual(' INDEX  \\b MainBookmark \\f A', index.get_field_code())
# На новой странице начните закладку с именем, которое соответствует значению
# свойства "BookmarkName" поля INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.start_bookmark('MainBookmark')
# Поле INDEX подхватит эту запись, потому что она находится внутри закладки,
# и её тип записи также совпадает с типом записи поля INDEX.
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 1'
index_entry.entry_type = 'A'
self.assertEqual(' XE  "Index entry 1" \\f A', index_entry.get_field_code())
# Вставьте поле XE, которое не появится в INDEX, потому что типы записей не совпадают.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 2'
index_entry.entry_type = 'B'
# Закончите закладку и вставьте поле XE после неё.
# Оно того же типа, что и поле INDEX, но не будет отображаться
# поскольку он находится за пределами границ закладки.
builder.end_bookmark('MainBookmark')
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Index entry 3'
index_entry.entry_type = 'A'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Filtering.docx')
```

Shows how to populate an INDEX field with entries using XE fields, and also modify its appearance.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте поле INDEX, которое отобразит запись для каждого найденного в документе поля XE.
# Каждая запись будет отображать значение свойства Text поля XE слева,
# а номер страницы, содержащей поле XE, — справа.
# Если у полей XE одинаковое значение в их свойстве "Text",
# поле INDEX сгруппирует их в одну запись.
index = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX, update_field=True).as_field_index()
index.language_id = '1033'
# Установка значения этого свойства в "A" сгруппирует все записи по первой букве,
# и разместит эту букву в верхнем регистре над каждой группой.
index.heading = 'A'
# Установите, чтобы таблица, созданная полем INDEX, охватывала 2 столбца.
index.number_of_columns = '2'
# Установите, чтобы любые записи, начинающиеся с букв вне диапазона "a-c", были опущены.
index.letter_range = 'a-c'
self.assertEqual(' INDEX  \\z 1033 \\h A \\c 2 \\p a-c', index.get_field_code())
# Следующие два поля XE появятся под заголовком "A",
# при этом их соответствующее форматирование текста также будет применено к номерам страниц.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apple'
index_entry.is_italic = True
self.assertEqual(' XE  Apple \\i', index_entry.get_field_code())
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Apricot'
index_entry.is_bold = True
self.assertEqual(' XE  Apricot \\b', index_entry.get_field_code())
# Оба следующих поля XE будут под заголовками "B" и "C" в оглавлении таблицы полей INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Banana'
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Cherry'
# Поля INDEX сортируют все записи в алфавитном порядке, поэтому эта запись появится под "A" вместе с другими двумя.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Avocado'
# Эта запись не появится, потому что она начинается с буквы "D",
# что находится за пределами диапазона символов "a-c", определяемого свойством LetterRange поля INDEX.
builder.insert_break(aw.BreakType.PAGE_BREAK)
index_entry = builder.insert_field(field_type=aw.fields.FieldType.FIELD_INDEX_ENTRY, update_field=True).as_field_xe()
index_entry.text = 'Durian'
doc.update_page_layout()
doc.update_fields()
doc.save(file_name=ARTIFACTS_DIR + 'Field.INDEX.XE.Formatting.docx')
```

### See Also

* module [aspose.words.fields](../)
* class [Field](../field/)

