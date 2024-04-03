---
title: ImageSaveOptions class
linktitle: ImageSaveOptions class
articleTitle: ImageSaveOptions class
second_title: Aspose.Words for Python
description: "aspose.words.saving.ImageSaveOptions class. Allows to specify additional options when rendering document pages or shapes to images"
type: docs
weight: 390
url: /python-net/aspose.words.saving/imagesaveoptions/
---

## ImageSaveOptions class

Allows to specify additional options when rendering document pages or shapes to images.
To learn more, visit the [Specify Save Options](https://docs.aspose.com/words/python-net/specify-save-options/) documentation article.




**Inheritance:** [ImageSaveOptions](./) → [FixedPageSaveOptions](../fixedpagesaveoptions/) → [SaveOptions](../saveoptions/)

### Constructors
| Name | Description |
| --- | --- |
| [ImageSaveOptions(save_format)](./__init__/#saveformat) | Initializes a new instance of this class that can be used to save rendered images in the [SaveFormat.TIFF](../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../aspose.words/saveformat/#JPEG), [SaveFormat.EMF](../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../aspose.words/saveformat/#EPS), [SaveFormat.WEB_P](../../aspose.words/saveformat/#WEB_P) or [SaveFormat.SVG](../../aspose.words/saveformat/#SVG) format. |

### Properties

| Name | Description |
| --- | --- |
| [allow_embedding_post_script_fonts](../saveoptions/allow_embedding_post_script_fonts/) | Gets or sets a boolean value indicating whether to allow embedding fonts with PostScript outlines when embedding TrueType fonts in a document upon it is saved. The default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [color_mode](../fixedpagesaveoptions/color_mode/) | Gets or sets a value determining how colors are rendered.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [default_template](../saveoptions/default_template/) | Gets or sets path to default template (including filename). Default value for this property is **empty string** ().<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_3d_effects_rendering_mode](../saveoptions/dml_3d_effects_rendering_mode/) | Gets or sets a value determining how 3D effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_effects_rendering_mode](../saveoptions/dml_effects_rendering_mode/) | Gets or sets a value determining how DrawingML effects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [dml_rendering_mode](../saveoptions/dml_rendering_mode/) | Gets or sets a value determining how DrawingML shapes are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [export_generator_name](../saveoptions/export_generator_name/) | When ``True``, causes the name and version of Aspose.Words to be embedded into produced files. Default value is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [horizontal_resolution](./horizontal_resolution/) | Gets or sets the horizontal resolution for the generated images, in dots per inch. |
| [image_brightness](./image_brightness/) | Gets or sets the brightness for the generated images. |
| [image_color_mode](./image_color_mode/) | Gets or sets the color mode for the generated images. |
| [image_contrast](./image_contrast/) | Gets or sets the contrast for the generated images. |
| [image_size](./image_size/) | Gets or sets the size of a generated image in pixels. |
| [iml_rendering_mode](../saveoptions/iml_rendering_mode/) | Gets or sets a value determining how ink (InkML) objects are rendered.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [jpeg_quality](./jpeg_quality/) | Gets or sets a value determining the quality of the generated JPEG images. |
| [memory_optimization](../saveoptions/memory_optimization/) | Gets or sets value determining if memory optimization should be performed before saving the document. Default value for this property is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [metafile_rendering_options](./metafile_rendering_options/) | Allows to specify how metafiles are treated in the rendered output. |
| [numeral_format](../fixedpagesaveoptions/numeral_format/) | Gets or sets [NumeralFormat](../numeralformat/) used for rendering of numerals. European numerals are used by default.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [optimize_output](../fixedpagesaveoptions/optimize_output/) | Flag indicates whether it is required to optimize output. If this flag is set redundant nested canvases and empty canvases are removed, also neighbor glyphs with the same formatting are concatenated. Note: The accuracy of the content display may be affected if this property is set to ``True``.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_saving_callback](../fixedpagesaveoptions/page_saving_callback/) | Allows to control how separate pages are saved when a document is exported to fixed page format.<br>(Inherited from [FixedPageSaveOptions](../fixedpagesaveoptions/)) |
| [page_set](./page_set/) | Gets or sets the pages to render. Default is all the pages in the document. |
| [paper_color](./paper_color/) | Gets or sets the background (paper) color for the generated images. The default value is aspose.pydrawing.Color.white. |
| [pixel_format](./pixel_format/) | Gets or sets the pixel format for the generated images. |
| [pretty_format](../saveoptions/pretty_format/) | When ``True``, pretty formats output where applicable. Default value is ``False``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [progress_callback](../saveoptions/progress_callback/) | Called during saving a document and accepts data about saving progress.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [save_format](./save_format/) | Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster [SaveFormat.TIFF](../../aspose.words/saveformat/#TIFF), [SaveFormat.PNG](../../aspose.words/saveformat/#PNG), [SaveFormat.BMP](../../aspose.words/saveformat/#BMP), [SaveFormat.JPEG](../../aspose.words/saveformat/#JPEG) or vector [SaveFormat.EMF](../../aspose.words/saveformat/#EMF), [SaveFormat.EPS](../../aspose.words/saveformat/#EPS), [SaveFormat.WEB_P](../../aspose.words/saveformat/#WEB_P), [SaveFormat.SVG](../../aspose.words/saveformat/#SVG). |
| [scale](./scale/) | Gets or sets the zoom factor for the generated images. |
| [temp_folder](../saveoptions/temp_folder/) | Specifies the folder for temporary files used when saving to a DOC or DOCX file. By default this property is ``None`` and no temporary files are used.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [threshold_for_floyd_steinberg_dithering](./threshold_for_floyd_steinberg_dithering/) | Gets or sets the threshold that determines the value of the binarization error in the Floyd-Steinberg method. when [ImageBinarizationMethod](../imagebinarizationmethod/) is [ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING](../imagebinarizationmethod/#FLOYD_STEINBERG_DITHERING). |
| [tiff_binarization_method](./tiff_binarization_method/) | Gets or sets method used while converting images to 1 bpp format when [ImageSaveOptions.save_format](./save_format/) is [SaveFormat.TIFF](../../aspose.words/saveformat/#TIFF) and [ImageSaveOptions.tiff_compression](./tiff_compression/) is equal to [TiffCompression.CCITT3](../tiffcompression/#CCITT3) or [TiffCompression.CCITT4](../tiffcompression/#CCITT4). |
| [tiff_compression](./tiff_compression/) | Gets or sets the type of compression to apply when saving generated images to the TIFF format. |
| [update_created_time_property](../saveoptions/update_created_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.created_time](../../aspose.words.properties/builtindocumentproperties/created_time/) property is updated before saving. Default value is ``False``;<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_fields](../saveoptions/update_fields/) | Gets or sets a value determining if fields of certain types should be updated before saving the document to a fixed page format. Default value for this property is ``True``.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_printed_property](../saveoptions/update_last_printed_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_printed](../../aspose.words.properties/builtindocumentproperties/last_printed/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [update_last_saved_time_property](../saveoptions/update_last_saved_time_property/) | Gets or sets a value determining whether the [BuiltInDocumentProperties.last_saved_time](../../aspose.words.properties/builtindocumentproperties/last_saved_time/) property is updated before saving.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_anti_aliasing](../saveoptions/use_anti_aliasing/) | Gets or sets a value determining whether or not to use anti-aliasing for rendering.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [use_gdi_emf_renderer](./use_gdi_emf_renderer/) | Gets or sets a value determining whether to use GDI+ or Aspose.Words metafile renderer when saving to EMF. |
| [use_high_quality_rendering](../saveoptions/use_high_quality_rendering/) | Gets or sets a value determining whether or not to use high quality (i.e. slow) rendering algorithms.<br>(Inherited from [SaveOptions](../saveoptions/)) |
| [vertical_resolution](./vertical_resolution/) | Gets or sets the vertical resolution for the generated images, in dots per inch. |

### Methods

| Name | Description |
| --- | --- |
|[ clone()](./clone/#default) | Creates a deep clone of this object. |
|[ create_save_options(save_format)](../saveoptions/create_save_options/#saveformat) | Creates a save options object of a class suitable for the specified save format.<br>(Inherited from [SaveOptions](../saveoptions/)) |
|[ create_save_options(file_name)](../saveoptions/create_save_options/#str) | Creates a save options object of a class suitable for the file extension specified in the given file name.<br>(Inherited from [SaveOptions](../saveoptions/)) |

### Examples

Renders a page of a Word document into an image with transparent or colored background.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Times New Roman"
builder.font.size = 24
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
img_options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)

# Set the "paper_color" property to a transparent color to apply a transparent
# background to the document while rendering it to an image.
img_options.paper_color = drawing.Color.transparent

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.paper_color.transparent.png", img_options)

# Set the "paper_color" property to an opaque color to apply that color
# as the background of the document as we render it to an image.
img_options.paper_color = drawing.Color.light_coral

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.paper_color.light_coral.png", img_options)
```

Shows how to configure compression while saving a document as a JPEG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)
builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
image_options = aw.saving.ImageSaveOptions(aw.SaveFormat.JPEG)

# Set the "jpeg_quality" property to "10" to use stronger compression when rendering the document.
# This will reduce the file size of the document, but the image will display more prominent compression artifacts.
image_options.jpeg_quality = 10

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_compression.jpg", image_options)

self.assertGreater(20000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_compression.jpg"))

# Set the "jpeg_quality" property to "100" to use weaker compression when rending the document.
# This will improve the quality of the image at the cost of an increased file size.
image_options.jpeg_quality = 100

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_quality.jpg", image_options)

self.assertLess(40000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.jpeg_quality.high_quality.jpg"))
```

Shows how to specify a resolution while rendering a document to PNG.

```python
doc = aw.Document()
builder = aw.DocumentBuilder(doc)

builder.font.name = "Times New Roman"
builder.font.size = 24
builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.")

builder.insert_image(IMAGE_DIR + "Logo.jpg")

# Create an "ImageSaveOptions" object which we can pass to the document's "save" method
# to modify the way in which that method renders the document into an image.
options = aw.saving.ImageSaveOptions(aw.SaveFormat.PNG)

# Set the "resolution" property to "72" to render the document in 72dpi.
options.vertical_resolution = 72
options.horizontal_resolution = 72

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.resolution.72dpi.png", options)

self.assertGreater(120000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.resolution.72dpi.png"))

image = drawing.Image.from_file(ARTIFACTS_DIR + "ImageSaveOptions.resolution.72dpi.png")

self.assertEqual(612, image.width)
self.assertEqual(792, image.height)

# Set the "resolution" property to "300" to render the document in 300dpi.
options.vertical_resolution = 300
options.horizontal_resolution = 300

doc.save(ARTIFACTS_DIR + "ImageSaveOptions.resolution.300dpi.png", options)

self.assertLess(700000, os.path.getsize(ARTIFACTS_DIR + "ImageSaveOptions.resolution.300dpi.png"))

image = drawing.Image.from_file(ARTIFACTS_DIR + "ImageSaveOptions.resolution.300dpi.png")

self.assertEqual(2550, image.width)
self.assertEqual(3300, image.height)
```

### See Also

* module [aspose.words.saving](../)
* class [FixedPageSaveOptions](../fixedpagesaveoptions/)

