---
title: ImageSaveOptions.page_layout property
linktitle: page_layout property
articleTitle: page_layout property
second_title: Aspose.Words for Python
description: "ImageSaveOptions.page_layout property. Gets or sets the layout used when rendering multiple pages into a single output."
type: docs
weight: 90
url: /python-net/aspose.words.saving/imagesaveoptions/page_layout/
---

## ImageSaveOptions.page_layout property

Gets or sets the layout used when rendering multiple pages into a single output.


```python
@property
def page_layout(self) -> aspose.words.saving.MultiPageLayout:
    ...

@page_layout.setter
def page_layout(self, value: aspose.words.saving.MultiPageLayout):
    ...

```

### Remarks

Use one of the factory methods of [MultiPageLayout](../../multipagelayout/) to configure this property.


For [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF) the default value is [MultiPageLayout.tiff_frames()](../../multipagelayout/tiff_frames/#default).
For other formats the default value is [MultiPageLayout.single_page()](../../multipagelayout/single_page/#default).


This property has effect only when saving to the following formats:
[SaveFormat.JPEG](../../../aspose.words/saveformat/#JPEG), [SaveFormat.GIF](../../../aspose.words/saveformat/#GIF), [SaveFormat.PNG](../../../aspose.words/saveformat/#PNG),
[SaveFormat.BMP](../../../aspose.words/saveformat/#BMP), [SaveFormat.TIFF](../../../aspose.words/saveformat/#TIFF), [SaveFormat.WEB_P](../../../aspose.words/saveformat/#WEB_P)





### Examples

Shows how to save the document into JPG image with multi-page layout settings.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)
# Set up a grid layout with:
# - 3 columns per row.
# - 10pts spacing between pages (horizontal and vertical).
options.page_layout = aw.saving.MultiPageLayout.grid(3, 10, 10)
# Alternative layouts:
# options.PageLayout = MultiPageLayout.Horizontal(10);
# options.PageLayout = MultiPageLayout.Vertical(10);
# Customize the background and border.
options.page_layout.back_color = aspose.pydrawing.Color.light_gray
options.page_layout.border_color = aspose.pydrawing.Color.blue
options.page_layout.border_width = 2
doc.save(file_name=ARTIFACTS_DIR + 'ImageSaveOptions.GridLayout.jpg', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [ImageSaveOptions](../)

