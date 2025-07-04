---
title: Aspose::Words::BorderCollection::get_DistanceFromText method
linktitle: get_DistanceFromText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::get_DistanceFromText method. Gets or sets distance of the border from text in points in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection::get_DistanceFromText method


Gets or sets distance of the border from text in points.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```

## Remarks


Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.

## Examples



Shows how to create green wavy page border with a shadow. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorders.docx");
```

## See Also

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
