---
title: PageSet constructor
linktitle: PageSet constructor
articleTitle: PageSet constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageSet constructor"
type: docs
weight: 10
url: /fr/python-net/aspose.words.saving/pageset/__init__/
---

## PageSet(page) {#int}

Creates an one-page set based on exact page index.


```python
def __init__(self, page: int):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| page | int | Zero-based index of the page. |

### Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering.
int.MaxValue C# constant means the last page in the document.



## PageSet(pages) {#intlist}

Creates a page set based on exact page indices.


```python
def __init__(self, pages: List[int]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| pages | List[int] | Zero-based indices of pages. |

### Remarks

If a page is encountered that is not in the document, an exception will be thrown during rendering.
int.MaxValue C# constant means the last page in the document.



## PageSet(ranges) {#pagerangelist}

Creates a page set based on ranges.


```python
def __init__(self, ranges: List[aspose.words.saving.PageRange]):
    ...
```

| Parameter | Type | Description |
| --- | --- | --- |
| ranges | List[[PageRange](../../pagerange/)] | Array of page ranges. |

### Remarks

If a range is encountered that starts after the last page in the document, 
an exception will be thrown during rendering.
All ranges that end after the last page are truncated to fit in the document.


## Examples

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
# Créez un objet "ImageSaveOptions" que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode rend le document en image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Définissez "PageSet" sur "1" pour sélectionner la deuxième page via
# l'index basé sur zéro à partir duquel commencer le rendu du document.
options.page_set = aw.saving.PageSet(page=1)
# Lorsque nous enregistrons le document au format JPEG, Aspose.Words ne rend qu'une seule page.
# Cette image contiendra une page à partir de la page deux,
# qui sera simplement la deuxième page du document original.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Ajoutez cinq pages au document.
i = 1
while i < 6:
    builder.write('Page ' + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Créez un objet "XpsSaveOptions", que nous pouvons transmettre à la méthode "Save" du document
# pour modifier la façon dont cette méthode convertit le document en .XPS.
xps_options = aw.saving.XpsSaveOptions()
# Utilisez la propriété "PageSet" pour sélectionner un ensemble de pages du document à enregistrer dans le XPS de sortie.
# Dans ce cas, nous choisirons, via un indice zéro, uniquement trois pages : page 1, page 2 et page 4.
xps_options.page_set = aw.saving.PageSet(pages=[0, 1, 3])
doc.save(file_name=ARTIFACTS_DIR + 'XpsSaveOptions.ExportExactPages.xps', save_options=xps_options)
```

Shows how to extract pages based on exact page ranges.

```python
doc = aw.Document(file_name=MY_DIR + 'Images.docx')
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
page_set = aw.saving.PageSet(ranges=[aw.saving.PageRange(1, 1), aw.saving.PageRange(2, 3), aw.saving.PageRange(1, 3), aw.saving.PageRange(2, 4), aw.saving.PageRange(1, 1)])
image_options.page_set = page_set
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.ExportVariousPageRanges.tiff', save_options=image_options)
```

## See Also

* module [aspose.words.saving](../../)
* class [PageSet](../)

