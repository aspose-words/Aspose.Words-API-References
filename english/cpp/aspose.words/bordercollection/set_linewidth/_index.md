---
title: Aspose::Words::BorderCollection::set_LineWidth method
linktitle: set_LineWidth
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::set_LineWidth method. Sets the border width in points in C++.'
type: docs
weight: 23000
url: /cpp/aspose.words/bordercollection/set_linewidth/
---
## BorderCollection::set_LineWidth method


Sets the border width in points.

```cpp
void Aspose::Words::BorderCollection::set_LineWidth(double value)
```

## Remarks


Returns the width of the first border in the collection.

Sets the width of all borders in the collection excluding diagonal borders.
## Examples


Shows how to create green wavy page border with a shadow.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(LineStyle::DoubleWave);
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
