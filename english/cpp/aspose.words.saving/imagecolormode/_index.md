---
title: Aspose::Words::Saving::ImageColorMode enum
linktitle: ImageColorMode
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageColorMode enum. Specifies the color mode for the generated images of document pages in C++.'
type: docs
weight: 64000
url: /cpp/aspose.words.saving/imagecolormode/
---
## ImageColorMode enum


Specifies the color mode for the generated images of document pages.

```cpp
enum class ImageColorMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| None | 0 | The pages of the document will be rendered as color images. |
| Grayscale | 1 | The pages of the document will be rendered as grayscale images. |
| BlackAndWhite | 2 | The pages of the document will be rendered as black and white images. |


## Examples



Shows how to set a color mode when rendering documents. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_ParagraphFormat()->set_Style(doc->get_Styles()->idx_get(u"Heading 1"));
builder->Writeln(u"Hello world!");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

// When we save the document as an image, we can pass a SaveOptions object to
// select a color mode for the image that the saving operation will generate.
// If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
// the saving operation will apply grayscale color reduction while rendering the document.
// If we set the "ImageColorMode" property to "ImageColorMode.Grayscale",
// the saving operation will render the document into a monochrome image.
// If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
// and preserve all the document's colors in the output image.
auto imageSaveOptions = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Png);
imageSaveOptions->set_ImageColorMode(imageColorMode);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.ColorMode.png", imageSaveOptions);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
