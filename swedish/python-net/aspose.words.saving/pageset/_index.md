---
title: PageSet class
linktitle: PageSet class
articleTitle: PageSet class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageSet class. Describes a random set of pages"
type: docs
weight: 600
url: /sv/python-net/aspose.words.saving/pageset/
---

## PageSet class

Describes a random set of pages.
To learn more, visit the [Programming with Documents](https://docs.aspose.com/words/python-net/programming-with-documents/) documentation article.




### Constructors
| Name | Description |
| --- | --- |
| [PageSet(page)](./__init__/#int) | Creates an one-page set based on exact page index. |
| [PageSet(pages)](./__init__/#intlist) | Creates a page set based on exact page indices. |
| [PageSet(ranges)](./__init__/#pagerangelist) | Creates a page set based on ranges. |

### Properties

| Name | Description |
| --- | --- |
| [all](./all/) | Gets a set with all the pages of the document in their original order. |
| [even](./even/) | Gets a set with all the even pages of the document in their original order. |
| [odd](./odd/) | Gets a set with all the odd pages of the document in their original order. |

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

### See Also

* module [aspose.words.saving](../)

