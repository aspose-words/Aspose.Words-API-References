---
title: PageSet constructor
linktitle: PageSet constructor
articleTitle: PageSet constructor
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageSet constructor"
type: docs
weight: 10
url: /sv/python-net/aspose.words.saving/pageset/__init__/
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
# Skapa ett "ImageSaveOptions"‑objekt som vi kan skicka till dokumentets "Save"‑metod
# för att ändra hur den metoden renderar dokumentet till en bild.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Ställ in "PageSet" till "1" för att välja den andra sidan via
# det nollbaserade indexet för att börja rendera dokumentet från.
options.page_set = aw.saving.PageSet(page=1)
# När vi sparar dokumentet i JPEG‑formatet renderar Aspose.Words bara en sida.
# Denna bild kommer att innehålla en sida som börjar från sida två,
# vilken bara är den andra sidan i det ursprungliga dokumentet.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

Shows how to extract pages based on exact page indices.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc=doc)
# Lägg till fem sidor i dokumentet.
i = 1
while i < 6:
    builder.write('Page ' + str(i))
    builder.insert_break(aw.BreakType.PAGE_BREAK)
    i += 1
# Skapa ett "XpsSaveOptions"-objekt, som vi kan skicka till dokumentets "Save"-metod
# för att ändra hur den metoden konverterar dokumentet till .XPS.
xps_options = aw.saving.XpsSaveOptions()
# Använd egenskapen "PageSet" för att välja en uppsättning av dokumentets sidor att spara till utdata‑XPS.
# I det här fallet kommer vi, via ett nollbaserat index, att välja endast tre sidor: sida 1, sida 2 och sida 4.
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

