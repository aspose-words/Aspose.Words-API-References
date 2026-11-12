---
title: ImageSaveOptions.page_set property
linktitle: page_set property
articleTitle: page_set property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.page_set property. Gets or sets the pages to render"
type: docs
weight: 100
url: /ru/python-net/aspose.words.saving/imagesaveoptions/page_set/
---

## ImageSaveOptions.page_set property

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

### Remarks

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.




### Examples

Shows how to render one page from a document to a JPEG image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(file_name=IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Создайте объект "ImageSaveOptions", который мы можем передать методу "Save" документа
# чтобы изменить способ, которым этот метод преобразует документ в изображение.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Установите "PageSet" в "1", чтобы выбрать вторую страницу через
# ноль‑базовый индекс, с которого начинать рендеринг документа.
options.page_set = aw.saving.PageSet(page=1)
# При сохранении документа в формате JPEG, Aspose.Words рендерит только одну страницу.
# Это изображение будет содержать одну страницу, начиная со второй страницы,
# которая будет просто второй страницей оригинального документа.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to specify which page in a document to render as an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
builder.paragraph_format.style = doc.styles.get_by_name('Heading 1')
builder.writeln('Hello world! This is page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('This is page 2.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('This is page 3.')
self.assertEqual(3, doc.page_count)
# При сохранении документа в виде изображения Aspose.Words по умолчанию рендерит только первую страницу.
# Мы можем передать объект SaveOptions, чтобы указать другую страницу для рендеринга.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.GIF)
# Отрендерите каждую страницу документа в отдельный файл изображения.
i = 1
while i <= doc.page_count:
    save_options.page_set = aw.saving.PageSet(page=1)
    doc.save(file_name=ARTIFACTS_DIR + f'ImageSaveOptions.PageIndex.Page {i}.gif', save_options=save_options)
    i += 1
```

Shows how to extract pages based on exact page ranges.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
page_set = aw.saving.PageSet(ranges=[aw.saving.PageRange(1, 1), aw.saving.PageRange(2, 3), aw.saving.PageRange(1, 3), aw.saving.PageRange(2, 4), aw.saving.PageRange(1, 1)])
image_options.page_set = page_set
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ExportVariousPageRanges.tiff', save_options=image_options)
```

Shows how to render every page of a document to a separate TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.writeln('Page 1.')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 2.')
builder.insert_image(IMAGE_DIR + 'Logo.jpg')
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln('Page 3.')
# Создайте объект "ImageSaveOptions", который мы можем передать методу "save" документа
# чтобы изменить способ, которым этот метод преобразует документ в изображение.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # Установите свойство "page_set" в номер первой страницы, с которой
    # начинается рендеринг документа.
    options.page_set = aw.saving.PageSet(i)
    options.vertical_resolution = 600
    options.horizontal_resolution = 600
    options.image_size = aspose.pydrawing.Size(2325, 5325)
    doc.save(ARTIFACTS_DIR + f'ImageSaveOptions.page_by_page.{i + 1}.tiff', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

