---
title: MultiPageLayout class
linktitle: MultiPageLayout class
articleTitle: MultiPageLayout class
second_title: Aspose.Words for Python
description: "aspose.words.saving.MultiPageLayout class. Defines a layout for rendering multiple pages into a single output."
type: docs
weight: 510
url: /python-net/aspose.words.saving/multipagelayout/
---

## MultiPageLayout class

Defines a layout for rendering multiple pages into a single output.


### Remarks

Use one of the static factory methods to create a layout configuration.


### Properties

| Name | Description |
| --- | --- |
| [back_color](./back_color/) | Gets or sets the background color of the output. The default is aspose.pydrawing.Color.empty. |
| [border_color](./border_color/) | Gets or sets the color of the pages border. The default is aspose.pydrawing.Color.empty. |
| [border_width](./border_width/) | Gets or sets the width of the pages border. The default is 0. |

### Methods

| Name | Description |
| --- | --- |
|[ grid(columns, horizontal_gap, vertical_gap)](./grid/#int_float_float) | Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns. |
|[ horizontal(horizontal_gap)](./horizontal/#float) | Creates a layout in which all specified pages are rendered horizontally side by side, left to right, in a single output. |
|[ single_page()](./single_page/#default) | Creates a layout that renders only the first of specified pages. |
|[ tiff_frames()](./tiff_frames/#default) | Creates a layout where each page is rendered as a separate frame in a multi-frame TIFF image. Applicable only to TIFF image formats. |
|[ vertical(vertical_gap)](./vertical/#float) | Creates a layout where all specified pages are rendered vertically one below the other in a single output. |

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

* module [aspose.words.saving](../)

