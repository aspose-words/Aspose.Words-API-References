---
title: PageSet class
linktitle: PageSet class
articleTitle: PageSet class
second_title: Aspose.Words for Python
description: "aspose.words.saving.PageSet class. Describes a random set of pages"
type: docs
weight: 600
url: /ar/python-net/aspose.words.saving/pageset/
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
# أنشئ كائن "ImageSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
# لتعديل الطريقة التي تقوم بها تلك الطريقة بتحويل المستند إلى صورة.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# عيّن "PageSet" إلى "1" لاختيار الصفحة الثانية عبر
# الفهرس الصفري للبدء في تحويل المستند من.
options.page_set = aw.saving.PageSet(page=1)
# عند حفظ المستند بتنسيق JPEG، تقوم Aspose.Words بتحويل صفحة واحدة فقط.
# ستحتوي هذه الصورة على صفحة واحدة تبدأ من الصفحة الثانية،
# وهي ببساطة الصفحة الثانية من المستند الأصلي.
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.OnePage.jpg', save_options=options)
```

### See Also

* module [aspose.words.saving](../)

