---
title: PageSetup.rtl_gutter property
linktitle: rtl_gutter property
articleTitle: rtl_gutter property
second_title: Aspose.Words for Python
description: "PageSetup.rtl_gutter property. Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language."
type: docs
weight: 380
url: /ru/python-net/aspose.words/pagesetup/rtl_gutter/
---

## PageSetup.rtl_gutter property

Gets or sets whether Microsoft Word uses gutters for the section based on a right-to-left language or a left-to-right language.


```python
@property
def rtl_gutter(self) -> bool:
    ...

@rtl_gutter.setter
def rtl_gutter(self, value: bool):
    ...

```

### Examples

Shows how to set gutter margins.

```python
doc = aw.Document()
# Вставьте текст, охватывающий несколько страниц.
builder = aw.DocumentBuilder(doc=doc)
i = 0
while i < 6:
    builder.write('Lorem ipsum dolor sit amet, consectetur adipiscing elit, ' + 'sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.')
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Внутренний отступ добавляет пробелы к левому или правому полю страницы,
# что компенсирует центральное сгибание страниц в книге, вторгающееся в макет страницы.
page_setup = doc.sections[0].page_setup
# Определите, сколько места наши страницы имеют для текста внутри полей, а затем добавьте значение для заполнения поля.
self.assertAlmostEqual(470.3, page_setup.page_width - page_setup.left_margin - page_setup.right_margin, delta=0.01)
page_setup.gutter = 100
# Установите свойство "RtlGutter" в значение "true", чтобы разместить внутренний отступ в более подходящем положении для текста справа налево.
page_setup.rtl_gutter = True
# Установите свойство "MultiplePages" в "MultiplePagesType.MirrorMargins", чтобы чередовать
# позицию левого/правого поля на каждой странице.
page_setup.multiple_pages = aw.settings.MultiplePagesType.MIRROR_MARGINS
doc.save(file_name=ARTIFACTS_DIR + 'PageSetup.Gutter.docx')
```

### See Also

* module [aspose.words](../../)
* class [PageSetup](../)

