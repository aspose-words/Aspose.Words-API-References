---
title: MillimeterToPoint
second_title: Aspose.Words for C++ API Reference
description: Converts millimeters to points.
type: docs
weight: 14
url: /cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil.MillimeterToPoint method


Converts millimeters to points.

```cpp
static double Aspose::Words::ConvertUtil::MillimeterToPoint(double millimeters)
```


| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | double | The value to convert. |

## Examples




Shows how to specify page properties in millimeters. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a more familiar measurement unit,
// such as millimeters when defining boundaries.
SharedPtr<PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(ConvertUtil::MillimeterToPoint(40));

// A centimeter is approximately 28.3 points.
ASSERT_NEAR(28.34, ConvertUtil::MillimeterToPoint(10), 0.01);

// Add content to demonstrate the new margins.
builder->Writeln(String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) +
                 String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) +
                 String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) +
                 String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(ArtifactsDir + u"UtilityClasses.PointsAndMillimeters.docx");
```

