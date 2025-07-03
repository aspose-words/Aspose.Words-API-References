---
title: Aspose::Words::ConvertUtil::PixelToNewDpi method
linktitle: PixelToNewDpi
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ConvertUtil::PixelToNewDpi method. Converts pixels from one resolution to another in C++.'
type: docs
weight: 3000
url: /cpp/aspose.words/convertutil/pixeltonewdpi/
---
## ConvertUtil::PixelToNewDpi method


Converts pixels from one resolution to another.

```cpp
static int32_t Aspose::Words::ConvertUtil::PixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |
| oldDpi | double | The current dpi (dots per inch) resolution. |
| newDpi | double | The new dpi (dots per inch) resolution. |

## Examples



Shows how to use convert points to pixels with default and custom resolution. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Define the size of the top margin of this section in pixels, according to a custom DPI.
const double myDpi = 192;

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// At the default DPI of 96, a pixel is 0.75 points.
ASPOSE_ASSERT_EQ(0.75, Aspose::Words::ConvertUtil::PixelToPoint(1));

builder->Writeln(System::String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + System::String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Set a new DPI and adjust the top margin value accordingly.
const double newDpi = 300;
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(System::String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(), Aspose::Words::ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) + u"pixels from the top of the page.");

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## See Also

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
