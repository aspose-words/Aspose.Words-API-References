---
title: FixedPageSaveOptions.page_set property
linktitle: page_set property
articleTitle: page_set property
second_title: Aspose.Words for Python
description: "FixedPageSaveOptions.page_set property. Gets or sets the pages to render"
type: docs
weight: 70
url: /ru/python-net/aspose.words.saving/fixedpagesaveoptions/page_set/
---

## FixedPageSaveOptions.page_set property

Gets or sets the pages to render.
Default is all the pages in the document.


```python
@property
def page_set(self) -> aspose.words.saving.PageSet:
    ...

@page_set.setter
def page_set(self, value: aspose.words.saving.PageSet):
    ...

```

### Examples

Shows how to export Odd pages from the document.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 5:
    builder.writeln(f"Page {i + 1} ({('odd' if i % 2 == 0 else 'even')})")
    if i < 4:
        builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Создайте объект "PdfSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод конвертирует документ в .PDF.
options = aw.saving.PdfSaveOptions()
# Ниже приведены три свойства PageSet, которые мы можем использовать для фильтрации набора страниц из
# нашего документа для сохранения в выходном PDF‑документе в зависимости от чётности их номеров страниц.
# 1 -  Сохранить только чётные страницы:
options.page_set = aw.saving.PageSet.even
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Even.pdf', save_options=options)
# 2 -  Сохранить только нечётные страницы:
options.page_set = aw.saving.PageSet.odd
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.Odd.pdf', save_options=options)
# 3 -  Сохранить каждую страницу:
options.page_set = aw.saving.PageSet.all
doc.save(file_name=ARTIFACTS_DIR + 'PdfSaveOptions.ExportPageSet.All.pdf', save_options=options)
```

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Добавьте пять страниц в документ.
i = 1
while i < 6:
    builder.write('Page ' + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Создайте объект "XpsSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в .XPS.
xps_options = aw.saving.XpsSaveOptions()
# Используйте свойство "PageSet", чтобы выбрать набор страниц документа для сохранения в выходной XPS.
# В этом случае мы выберем, используя нулевой индекс, только три страницы: страницу 1, страницу 2 и страницу 4.
xps_options.page_set = aw.saving.PageSet(pages=[0, 1, 3])
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.ExportExactPages.xps', save_options=xps_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [FixedPageSaveOptions](../)

