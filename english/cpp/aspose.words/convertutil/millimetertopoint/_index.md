---
title: Aspose::Words::ConvertUtil::MillimeterToPoint method
linktitle: MillimeterToPoint
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ConvertUtil::MillimeterToPoint method. Converts millimeters to points in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words/convertutil/millimetertopoint/
---
## ConvertUtil::MillimeterToPoint method


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
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a more familiar measurement unit,
// such as millimeters when defining boundaries.
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(30));
pageSetup->set_BottomMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(50));
pageSetup->set_LeftMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(80));
pageSetup->set_RightMargin(Aspose::Words::ConvertUtil::MillimeterToPoint(40));

// A centimeter is approximately 28.3 points.
ASSERT_NEAR(28.34, Aspose::Words::ConvertUtil::MillimeterToPoint(10), 0.01);

// Add content to demonstrate the new margins.
builder->Writeln(System::String::Format(u"This Text is {0} points from the left, ", pageSetup->get_LeftMargin()) + System::String::Format(u"{0} points from the right, ", pageSetup->get_RightMargin()) + System::String::Format(u"{0} points from the top, ", pageSetup->get_TopMargin()) + System::String::Format(u"and {0} points from the bottom of the page.", pageSetup->get_BottomMargin()));

doc->Save(get_ArtifactsDir() + u"UtilityClasses.PointsAndMillimeters.docx");
```

## See Also

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
