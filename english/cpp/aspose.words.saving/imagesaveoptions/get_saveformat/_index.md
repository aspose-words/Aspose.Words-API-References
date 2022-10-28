---
title: get_SaveFormat
second_title: Aspose.Words for C++ API Reference
description: Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster Tiff, Png, Bmp, Jpeg or vector Emf, Svg.
type: docs
weight: 144
url: /cpp/aspose.words.saving/imagesaveoptions/get_saveformat/
---
## ImageSaveOptions.get_SaveFormat method


Specifies the format in which the rendered document pages or shapes will be saved if this save options object is used. Can be a raster **Tiff**, **Png**, **Bmp**, **Jpeg** or vector **Emf**, **Svg**.

```cpp
Aspose::Words::SaveFormat Aspose::Words::Saving::ImageSaveOptions::get_SaveFormat() override
```


On different platforms, the supported formats may be different. The number of other options depends on the selected format.

Also, it is possible to save to SVG both via [ImageSaveOptions](../) and via [SvgSaveOptions](../../svgsaveoptions/).

## Examples




Shows how to edit the image while Aspose.Words converts a document to one. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(ImageDir + u"Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// edit the image while the saving operation renders it.
auto options = MakeObject<ImageSaveOptions>(SaveFormat::Png);
options->set_ImageBrightness(0.3f);
options->set_ImageContrast(0.7f);
options->set_HorizontalResolution(72.f);
options->set_VerticalResolution(72.f);
options->set_Scale(96.f / 72.f);

doc->Save(ArtifactsDir + u"ImageSaveOptions.EditImage.png", options);
```

