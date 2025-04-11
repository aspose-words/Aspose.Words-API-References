---
title: HtmlSaveOptions.image_resolution property
linktitle: image_resolution property
articleTitle: image_resolution property
second_title: Aspose.Words for Python
description: "HtmlSaveOptions.image_resolution property. Specifies the output resolution for images when exporting to HTML, MHTML or EPUB"
type: docs
weight: 340
url: /python-net/aspose.words.saving/htmlsaveoptions/image_resolution/
---

## HtmlSaveOptions.image_resolution property

Specifies the output resolution for images when exporting to HTML, MHTML or EPUB.
Default is ``96 dpi``.



```python
@property
def image_resolution(self) -> int:
    ...

@image_resolution.setter
def image_resolution(self, value: int):
    ...

```

### Remarks

This property effects raster images when [HtmlSaveOptions.scale_image_to_shape_size](../scale_image_to_shape_size/)
is ``True`` and effects metafiles exported as raster images. Some image properties such as cropping
or rotation require saving transformed images and in this case transformed images are created in the given
resolution.




### Examples

Shows how to set folders and folder aliases for externally saved resources that Aspose.Words will create when saving a document to HTML.

```python
doc = aw.Document(file_name=MY_DIR + 'Rendering.docx')
options = aw.saving.HtmlSaveOptions()
options.css_style_sheet_type = aw.saving.CssStyleSheetType.EXTERNAL
options.export_font_resources = True
options.image_resolution = 72
options.font_resources_subsetting_size_threshold = 0
options.fonts_folder = ARTIFACTS_DIR + 'Fonts'
options.images_folder = ARTIFACTS_DIR + 'Images'
options.resource_folder = ARTIFACTS_DIR + 'Resources'
options.fonts_folder_alias = 'http://example.com/fonts'
options.images_folder_alias = 'http://example.com/images'
options.resource_folder_alias = 'http://example.com/resources'
options.export_original_url_for_linked_images = True
doc.save(file_name=ARTIFACTS_DIR + 'HtmlSaveOptions.FolderAlias.html', save_options=options)
```

### See Also

* module [aspose.words.saving](../../)
* class [HtmlSaveOptions](../)
* property [HtmlSaveOptions.scale_image_to_shape_size](../scale_image_to_shape_size/)

