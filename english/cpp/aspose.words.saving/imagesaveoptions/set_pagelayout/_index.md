---
title: Aspose::Words::Saving::ImageSaveOptions::set_PageLayout method
linktitle: set_PageLayout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::ImageSaveOptions::set_PageLayout method. Sets the layout used when rendering multiple pages into a single output in C++.'
type: docs
weight: 26500
url: /cpp/aspose.words.saving/imagesaveoptions/set_pagelayout/
---
## ImageSaveOptions::set_PageLayout method


Sets the layout used when rendering multiple pages into a single output.

```cpp
void Aspose::Words::Saving::ImageSaveOptions::set_PageLayout(const System::SharedPtr<Aspose::Words::Saving::MultiPageLayout> & value)
```

## Remarks


 Use one of the factory methods of [MultiPageLayout](../../multipagelayout/) to configure this property. 

 For [Tiff](../../../aspose.words/saveformat/) the default value is [TiffFrames](../../multipagelayout/tiffframes/). For other formats the default value is [SinglePage](../../multipagelayout/singlepage/). 

 This property has effect only when saving to the following formats: [Jpeg](../../../aspose.words/saveformat/), [Gif](../../../aspose.words/saveformat/), [Png](../../../aspose.words/saveformat/), [Bmp](../../../aspose.words/saveformat/), [Tiff](../../../aspose.words/saveformat/), **WebP**
## Examples


Shows how to save the document into JPG image with multi-page layout settings.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(System::String(get_MyDir() + u"Rendering.docx"));

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(SaveFormat::Jpeg);
// Set up a grid layout with:
// - 3 columns per row.
// - 10pts spacing between pages (horizontal and vertical).
options->set_PageLayout(MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Alternative layouts:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Customize the background and border.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```
## See Also

* Class [ImageSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
