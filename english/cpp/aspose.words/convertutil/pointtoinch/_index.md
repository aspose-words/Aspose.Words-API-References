---
title: Aspose::Words::ConvertUtil::PointToInch method
linktitle: PointToInch
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ConvertUtil::PointToInch method. Converts points to inches in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/convertutil/pointtoinch/
---
## ConvertUtil::PointToInch method


Converts points to inches.

```cpp
static double Aspose::Words::ConvertUtil::PointToInch(double points)
```


| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. |

## Examples



Shows how to specify page properties in inches. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// A section's "Page Setup" defines the size of the page margins in points.
// We can also use the "ConvertUtil" class to use a more familiar measurement unit,
// such as inches when defining boundaries.
SharedPtr<PageSetup> pageSetup = builder->get_PageSetup();
pageSetup->set_TopMargin(ConvertUtil::InchToPoint(1.0));
pageSetup->set_BottomMargin(ConvertUtil::InchToPoint(2.0));
pageSetup->set_LeftMargin(ConvertUtil::InchToPoint(2.5));
pageSetup->set_RightMargin(ConvertUtil::InchToPoint(1.5));

// An inch is 72 points.
ASPOSE_ASSERT_EQ(72.0, ConvertUtil::InchToPoint(1));
ASPOSE_ASSERT_EQ(1.0, ConvertUtil::PointToInch(72));

// Add content to demonstrate the new margins.
builder->Writeln(
    String::Format(u"This Text is {0} points/{1} inches from the left, ", pageSetup->get_LeftMargin(),
                   ConvertUtil::PointToInch(pageSetup->get_LeftMargin())) +
    String::Format(u"{0} points/{1} inches from the right, ", pageSetup->get_RightMargin(), ConvertUtil::PointToInch(pageSetup->get_RightMargin())) +
    String::Format(u"{0} points/{1} inches from the top, ", pageSetup->get_TopMargin(), ConvertUtil::PointToInch(pageSetup->get_TopMargin())) +
    String::Format(u"and {0} points/{1} inches from the bottom of the page.", pageSetup->get_BottomMargin(),
                   ConvertUtil::PointToInch(pageSetup->get_BottomMargin())));

doc->Save(ArtifactsDir + u"UtilityClasses.PointsAndInches.docx");
```

## See Also

* Class [ConvertUtil](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
