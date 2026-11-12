---
title: TxtListIndentation.count property
linktitle: count property
articleTitle: count property
second_title: Aspose.Words for Python
description: "TxtListIndentation.count property. Gets or sets how many [TxtListIndentation.character](../character/) to use as indentation per one list level"
type: docs
weight: 30
url: /ru/python-net/aspose.words.saving/txtlistindentation/count/
---

## TxtListIndentation.count property

Gets or sets how many [TxtListIndentation.character](../character/) to use as indentation per one list level.
The default value is 0, that means no indentation.



```python
@property
def count(self) -> int:
    ...

@count.setter
def count(self, value: int):
    ...

```

### Examples

Shows how to configure list indenting when saving a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Создайте список с тремя уровнями отступа.
builder.list_format.apply_number_default()
builder.writeln('Item 1')
builder.list_format.list_indent()
builder.writeln('Item 2')
builder.list_format.list_indent()
builder.write('Item 3')
# Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ сохранения документа в простой текст.
txt_save_options = aw.saving.TxtSaveOptions()
# Установите свойство "Character", чтобы задать символ для использования
# для заполнения, имитирующего отступ списка в обычном тексте.
txt_save_options.list_indentation.character = ' '
# Установите свойство "Count", чтобы указать количество раз
# для размещения символа заполнения на каждом уровне отступа списка.
txt_save_options.list_indentation.count = 3
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt', save_options=txt_save_options)
doc_text = system_helper.io.File.read_all_text(ARTIFACTS_DIR + 'TxtSaveOptions.TxtListIndentation.txt')
new_line = system_helper.environment.Environment.new_line()
self.assertEqual(f'1. Item 1{new_line}' + f'   a. Item 2{new_line}' + f'      i. Item 3{new_line}', doc_text)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtListIndentation](../)

