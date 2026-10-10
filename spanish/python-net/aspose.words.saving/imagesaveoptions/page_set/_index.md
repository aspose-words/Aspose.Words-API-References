---
title: ImageSaveOptions.page_set property
linktitle: page_set property
articleTitle: page_set property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.page_set property. Gets or sets the pages to render"
type: docs
weight: 100
url: /es/python-net/aspose.words.saving/imagesaveoptions/page_set/
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
# Cree un objeto "ImageSaveOptions" que podamos pasar al método "Save" del documento
# para modificar la forma en que ese método renderiza el documento en una imagen.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Establezca "PageSet" a "1" para seleccionar la segunda página mediante
# el índice basado en cero desde el cual comenzar a renderizar el documento.
options.page_set = aw.saving.PageSet(page=1)
# Al guardar el documento en formato JPEG, Aspose.Words solo renderiza una página.
# Esta imagen contendrá una página que comienza desde la página dos,
# que será simplemente la segunda página del documento original.
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
# Al guardar el documento como imagen, Aspose.Words solo renderiza la primera página de forma predeterminada.
# Podemos pasar un objeto SaveOptions para especificar una página diferente para renderizar.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.GIF)
# Renderiza cada página del documento a un archivo de imagen separado.
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
# Cree un objeto "ImageSaveOptions" que podamos pasar al método "save" del documento
# para modificar la forma en que ese método renderiza el documento en una imagen.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
for i in range(doc.page_count):
    # Establezca la propiedad "page_set" al número de la primera página desde
    # la cual comenzar a renderizar el documento.
    options.page_set = aw.saving.PageSet(i)
    options.vertical_resolution = 600
    options.horizontal_resolution = 600
    options.image_size = aspose.pydrawing.Size(2325, 5325)
    doc.save(ARTIFACTS_DIR + f'ImageSaveOptions.page_by_page.{i + 1}.tiff', options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

