---
title: Paragraph.list_label property
linktitle: list_label property
articleTitle: list_label property
second_title: Aspose.Words for Python
description: "Paragraph.list_label property. Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting for this paragraph."
type: docs
weight: 160
url: /ru/python-net/aspose.words/paragraph/list_label/
---

## Paragraph.list_label property

Gets a [Paragraph.list_label](./) object that provides access to list numbering value and formatting
for this paragraph.



```python
@property
def list_label(self) -> aspose.words.lists.ListLabel:
    ...

```

### Examples

Shows how to extract the list labels of all paragraphs that are list items.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
doc.update_list_labels()
paras = doc.get_child_nodes(aw.NodeType.PARAGRAPH, True)
# Найдите, есть ли у нас список абзацев. В нашем документе наш список использует простые арабские цифры,
# которые начинаются с трёх и заканчиваются на шести.
for paragraph in list(filter(lambda p: p.list_format.is_list_item, list(filter(lambda a: a is not None, map(lambda b: system_helper.linq.Enumerable.of_type(lambda x: x.as_paragraph(), b), list(paras)))))):
    print(f'List item paragraph #{paras.index_of(paragraph)}')
    # Это текст, который мы получаем, когда выводим этот узел в текстовый формат.
    # Этот вывод текста будет опускать метки списка. Удалите любые символы форматирования абзаца.
    paragraph_text = paragraph.to_string(save_format=aw.SaveFormat.TEXT).strip()
    print(f'\tExported Text: {paragraph_text}')
    label = paragraph.list_label
    # Это получает позицию абзаца на текущем уровне списка. Если у нас есть список с несколькими уровнями,
    # это покажет, какую позицию он занимает на этом уровне.
    print(f'\tNumerical Id: {label.label_value}')
    # Объедините их, чтобы включить метку списка вместе с текстом в выводе.
    print(f'\tList label combined with text: {label.label_string} {paragraph_text}')
```

### See Also

* module [aspose.words](../../)
* class [Paragraph](../)

