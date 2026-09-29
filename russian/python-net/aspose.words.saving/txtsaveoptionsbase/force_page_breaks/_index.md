---
title: TxtSaveOptionsBase.force_page_breaks property
linktitle: force_page_breaks property
articleTitle: force_page_breaks property
second_title: Aspose.Words for Python
description: "TxtSaveOptionsBase.force_page_breaks property. Allows to specify whether the page breaks should be preserved during export."
type: docs
weight: 30
url: /ru/python-net/aspose.words.saving/txtsaveoptionsbase/force_page_breaks/
---

## TxtSaveOptionsBase.force_page_breaks property

Allows to specify whether the page breaks should be preserved during export.

The default value is ``False``.




```python
@property
def force_page_breaks(self) -> bool:
    ...

@force_page_breaks.setter
def force_page_breaks(self, value: bool):
    ...

```

### Remarks

The property affects only page breaks that are inserted explicitly into a document. 
It is not related to page breaks that MS Word automatically inserts at the end of each page.


### Examples

Shows how to specify whether to preserve page breaks when exporting a document to plaintext.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3')
# Создайте объект "TxtSaveOptions", который мы можем передать методу "Save" документа
# метод для изменения способа сохранения документа в простой текст.
save_options = aw.saving.TxtSaveOptions()
# Объекты "Document" Aspose.Words имеют разрывы страниц, как и документы Microsoft Word.
# Форматы сохранения, такие как ".txt", представляют собой непрерывный текст без разрывов страниц.
# Установите свойство "ForcePageBreaks" в значение "true", чтобы сохранить все разрывы страниц в виде символов '\f'.
# Установите свойство "ForcePageBreaks" в значение "false", чтобы удалить все разрывы страниц.
save_options.force_page_breaks = force_page_breaks
doc.save(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt', save_options=save_options)
# Если мы загрузим простой текстовый документ с разрывами страниц,
# объект "Document" будет использовать их для разделения содержимого на страницы.
doc = aw.Document(file_name=ARTIFACTS_DIR + 'TxtSaveOptions.PageBreaks.txt')
self.assertEqual(3 if force_page_breaks else 1, doc.page_count)
```

### See Also

* module [aspose.words.saving](../../)
* class [TxtSaveOptionsBase](../)

