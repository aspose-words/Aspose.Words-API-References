---
title: Aspose::Words::BorderCollection::set_Color method
linktitle: set_Color
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::set_Color method. Sets the border color in C++.'
type: docs
weight: 20000
url: /cpp/aspose.words/bordercollection/set_color/
---
## BorderCollection::set_Color method


Sets the border color.

```cpp
void Aspose::Words::BorderCollection::set_Color(System::Drawing::Color value)
```

## Remarks


Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.
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
