---
title: get_VerticalResolution
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the vertical resolution for the generated images, in dots per inch.
type: docs
weight: 222
url: /cpp/aspose.words.saving/imagesaveoptions/get_verticalresolution/
---
## ImageSaveOptions::get_VerticalResolution method


Gets or sets the vertical resolution for the generated images, in dots per inch.

```cpp
float Aspose::Words::Saving::ImageSaveOptions::get_VerticalResolution() const
```

## Remarks


This property has effect only when saving to raster image formats and affects the output size in pixels.

The default value is 96.

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

## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words](../../../)
