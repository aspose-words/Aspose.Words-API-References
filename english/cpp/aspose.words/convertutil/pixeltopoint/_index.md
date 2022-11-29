---
title: PixelToPoint
second_title: Aspose.Words for C++ API Reference
description: Converts pixels to points at 96 dpi.
type: docs
weight: 40
url: /cpp/aspose.words/convertutil/pixeltopoint/
---
## ConvertUtil::PixelToPoint(double) method


Converts pixels to points at 96 dpi.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |

## Examples



Shows how to specify page properties in pixels. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a different measurement unit,
// such as pixels when defining boundaries.
SharedPtr<PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(ConvertUtil::PixelToPoint(100));
pageSetup->set_BottomMargin(ConvertUtil::PixelToPoint(200));
pageSetup->set_LeftMargin(ConvertUtil::PixelToPoint(225));
pageSetup->set_RightMargin(ConvertUtil::PixelToPoint(125));

// A pixel is 0.75 points.
ASPOSE_ASSERT_EQ(0.75, ConvertUtil::PixelToPoint(1));
ASPOSE_ASSERT_EQ(1.0, ConvertUtil::PointToPixel(0.75));

// The default DPI value used is 96.
ASPOSE_ASSERT_EQ(0.75, ConvertUtil::PixelToPoint(1, 96));

// Add content to demonstrate the new margins.
builder->Writeln(
    String::Format(u"This Text is {0} points/{1} pixels from the left, ", pageSetup->get_LeftMargin(),
                   ConvertUtil::PointToPixel(pageSetup->get_LeftMargin())) +
    String::Format(u"{0} points/{1} pixels from the right, ", pageSetup->get_RightMargin(), ConvertUtil::PointToPixel(pageSetup->get_RightMargin())) +
    String::Format(u"{0} points/{1} pixels from the top, ", pageSetup->get_TopMargin(), ConvertUtil::PointToPixel(pageSetup->get_TopMargin())) +
    String::Format(u"and {0} points/{1} pixels from the bottom of the page.", pageSetup->get_BottomMargin(),
                   ConvertUtil::PointToPixel(pageSetup->get_BottomMargin())));

doc->Save(ArtifactsDir + u"UtilityClasses.PointsAndPixels.docx");
```

## See Also

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
## ConvertUtil::PixelToPoint(double, double) method


Converts pixels to points at the specified pixel resolution.

```cpp
static double Aspose::Words::ConvertUtil::PixelToPoint(double pixels, double resolution)
```


| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |
| resolution | double | The dpi (dots per inch) resolution. |

## Examples



Shows how to use convert points to pixels with default and custom resolution. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Define the size of the top margin of this section in pixels, according to a custom DPI.
const double myDpi = 192;

SharedPtr<PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(ConvertUtil::PixelToPoint(100, myDpi));

ASSERT_NEAR(37.5, pageSetup->get_TopMargin(), 0.01);

// At the default DPI of 96, a pixel is 0.75 points.
ASPOSE_ASSERT_EQ(0.75, ConvertUtil::PixelToPoint(1));

builder->Writeln(
    String::Format(u"This Text is {0} points/{1} ", pageSetup->get_TopMargin(), ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) +
    String::Format(u"pixels (at a DPI of {0}) from the top of the page.", myDpi));

// Set a new DPI and adjust the top margin value accordingly.
const double newDpi = 300;
pageSetup->set_TopMargin(ConvertUtil::PixelToNewDpi(pageSetup->get_TopMargin(), myDpi, newDpi));
ASSERT_NEAR(59.0, pageSetup->get_TopMargin(), 0.01);

builder->Writeln(String::Format(u"At a DPI of {0}, the text is now {1} points/{2} ", newDpi, pageSetup->get_TopMargin(),
                                ConvertUtil::PointToPixel(pageSetup->get_TopMargin(), myDpi)) +
                 u"pixels from the top of the page.");

doc->Save(ArtifactsDir + u"UtilityClasses.PointsAndPixelsDpi.docx");
```

## See Also

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
