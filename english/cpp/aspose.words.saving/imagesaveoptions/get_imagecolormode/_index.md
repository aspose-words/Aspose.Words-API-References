---
title: Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode method
linktitle: get_ImageColorMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode method. Gets or sets the color mode for the generated images in C++.'
type: docs
weight: 6000
url: /cpp/aspose.words.saving/imagesaveoptions/get_imagecolormode/
---
## ImageSaveOptions::get_ImageColorMode method


Gets or sets the color mode for the generated images.

```cpp
Aspose::Words::Saving::ImageColorMode Aspose::Words::Saving::ImageSaveOptions::get_ImageColorMode() const
```

## Remarks


This property has effect only when saving to raster image formats.

The default value is [None](../../imagecolormode/).

## Examples



Shows how to set a color mode when rendering documents. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(ImageDir + u"Logo.jpg");

ASSERT_LT(20000, MakeObject<System::IO::FileInfo>(ImageDir + u"Logo.jpg")->get_Length());

// When we save the document as an image, we can pass a SaveOptions object to
// select a color mode for the image that the saving operation will generate.
// If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
// the saving operation will apply grayscale color reduction while rendering the document.
// If we set the "ImageColorMode" property to "ImageColorMode.Grayscale",
// the saving operation will render the document into a monochrome image.
// If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
// and preserve all the document's colors in the output image.
auto imageSaveOptions = MakeObject<ImageSaveOptions>(SaveFormat::Png);
imageSaveOptions->set_ImageColorMode(imageColorMode);

doc->Save(ArtifactsDir + u"ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

## See Also

* Enum [ImageColorMode](../../imagecolormode/)
* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
