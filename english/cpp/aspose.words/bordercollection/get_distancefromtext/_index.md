---
title: get_DistanceFromText
second_title: Aspose.Words for C++ API Reference
description: Gets or sets distance of the border from text in points.
type: docs
weight: 66
url: /cpp/aspose.words/bordercollection/get_distancefromtext/
---
## BorderCollection.get_DistanceFromText method


Gets or sets distance of the border from text in points.

```cpp
double Aspose::Words::BorderCollection::get_DistanceFromText()
```


Gets the distance from text for the first border.

Sets the distance from text for all borders in the collection excluding diagonal borders.

Has no effect and will be automatically reset to zero for borders of table cells.

## Examples




Shows how to create green wavy page border with a shadow. 
```cpp
auto doc = MakeObject<Document>();
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(ArtifactsDir + u"PageSetup.PageBorders.docx");
```

