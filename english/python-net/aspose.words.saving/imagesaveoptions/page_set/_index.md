---
title: page_set property
second_title: Aspose.Words for Python via .NET API Reference
description: "Gets or sets the pages to render"
type: docs
weight: 80
url: /python-net/aspose.words.saving/imagesaveoptions/page_set/
---

## ImageSaveOptions.page_set property

Gets or sets the pages to render.
Default is all the pages in the document.

This property has effect only when rendering document pages. This property is ignored when rendering shapes to images.




### Examples

Shows how to render one page from a document to a JPEG image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

# Set the "page_set" to "1" to select the second page via
# the zero-based index to start rendering the document from.
options.page_set = aw.saving.PageSet(1)

# When we save the document to the JPEG format, Aspose.Words only renders one page.
# This image will contain one page starting from page two,
# which will just be the second page of the original document.
doc.save(ARTIFACTS_DIR + "ImageSaveOptions.one_page.jpg", options)
```

Shows how to specify which page in a document to render as an image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.paragraph_format.style = doc.styles.get_by_name("Heading 1")
builder.writeln("Hello world! This is page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("This is page 2.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("This is page 3.")

self.assertEqual(3, doc.page_count)

# When we save the document as an image, Aspose.Words only renders the first page by default.
# We can pass a SaveOptions object to specify a different page to render.
save_options = aw.saving.ImageSaveOptions(aw.SaveFormat.GIF)

# Render every page of the document to a separate image file.
for i in range(1, doc.page_count + 1):
    save_options.page_set = aw.saving.PageSet(1)

    doc.save(ARTIFACTS_DIR + f"ImageSaveOptions.page_set.page {i}.gif", save_options)
```

Shows how to render every page of a document to a separate TIFF image.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.writeln("Page 1.")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 2.")
builder.insert_image(IMAGE_DIR + "Logo.jpg")
builder.insert_break(aw.BreakType.PAGE_BREAK)
builder.writeln("Page 3.")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)

for i in range(doc.page_count):

    # Set the "page_set" property to the number of the first page from
    # which to start rendering the document from.
    options.page_set = aw.saving.PageSet(i)

    doc.save(ARTIFACTS_DIR + f"ImageSaveOptions.page_by_page.{i + 1}.tiff", options)
```

Shows how to extract pages based on exact page ranges.

```python
doc = aw.Document(MY_DIR + "Images.docx")

image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.TIFF)
ranges = [
    aw.saving.PageRange(1, 1),
    aw.saving.PageRange(2, 3),
    aw.saving.PageRange(1, 3),
    aw.saving.PageRange(2, 4),
    aw.saving.PageRange(1, 1)
    ]
page_set = aw.saving.PageSet(ranges=ranges)

image_options.page_set = page_set
doc.save(ARTIFACTS_DIR + "ImageSaveOptions.export_various_page_ranges.tiff", image_options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

