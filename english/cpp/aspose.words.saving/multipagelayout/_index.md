---
title: Aspose::Words::Saving::MultiPageLayout class
linktitle: MultiPageLayout
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Saving::MultiPageLayout class. Defines a layout for rendering multiple pages into a single output in C++.'
type: docs
weight: 14500
url: /cpp/aspose.words.saving/multipagelayout/
---
## MultiPageLayout class


Defines a layout for rendering multiple pages into a single output.

```cpp
class MultiPageLayout : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [get_BackColor](./get_backcolor/)() | Gets the background color of the output. The default is **Empty**. |
| [get_BorderColor](./get_bordercolor/)() | Gets the color of the pages border. The default is **Empty**. |
| [get_BorderWidth](./get_borderwidth/)() const | Gets the width of the pages border. The default is 0. |
| [GetType](./gettype/)() const override |  |
| static [Grid](./grid/)(int32_t, float, float) | Creates a layout in which pages are rendered left-to-right, top-to-bottom, in a grid with the specified number of columns. |
| static [Horizontal](./horizontal/)(float) | Creates a layout in which all specified pages are rendered horizontally side by side, left to right, in a single output. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_BackColor](./set_backcolor/)(System::Drawing::Color) | Sets the background color of the output. The default is **Empty**. |
| [set_BorderColor](./set_bordercolor/)(System::Drawing::Color) | Sets the color of the pages border. The default is **Empty**. |
| [set_BorderWidth](./set_borderwidth/)(float) | Sets the width of the pages border. The default is 0. |
| static [SinglePage](./singlepage/)() | Creates a layout that renders only the first of specified pages. |
| static [TiffFrames](./tiffframes/)() | Creates a layout where each page is rendered as a separate frame in a multi-frame TIFF image. Applicable only to TIFF image formats. |
| static [Type](./type/)() |  |
| static [Vertical](./vertical/)(float) | Creates a layout where all specified pages are rendered vertically one below the other in a single output. |

## Examples



Shows how to save the document into JPG image with multi-page layout settings. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::ImageSaveOptions>(Aspose::Words::SaveFormat::Jpeg);
// Set up a grid layout with:
// - 3 columns per row.
// - 10pts spacing between pages (horizontal and vertical).
options->set_PageLayout(Aspose::Words::Saving::MultiPageLayout::Grid(3, 10.0f, 10.0f));

// Alternative layouts:
// options.PageLayout = MultiPageLayout.Horizontal(10);
// options.PageLayout = MultiPageLayout.Vertical(10);

// Customize the background and border.
options->get_PageLayout()->set_BackColor(System::Drawing::Color::get_LightGray());
options->get_PageLayout()->set_BorderColor(System::Drawing::Color::get_Blue());
options->get_PageLayout()->set_BorderWidth(2.0f);

doc->Save(get_ArtifactsDir() + u"ImageSaveOptions.GridLayout.jpg", options);
```

## See Also

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
