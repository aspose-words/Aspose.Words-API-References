---
title: ListLabel class
linktitle: ListLabel class
articleTitle: ListLabel class
second_title: Aspose.Words for Python
description: "aspose.words.lists.ListLabel class. Defines properties specific to a list label"
type: docs
weight: 40
url: /ru/python-net/aspose.words.lists/listlabel/
---

## ListLabel class

Defines properties specific to a list label.
To learn more, visit the [Working with Lists](https://docs.aspose.com/words/python-net/working-with-lists/) documentation article.




### Properties

| Name | Description |
| --- | --- |
| [font](./font/) | Gets the list label font. |
| [label_string](./label_string/) | Gets a string representation of list label. |
| [label_value](./label_value/) | Gets a numeric value for this label. |

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

* module [aspose.words.lists](../)

