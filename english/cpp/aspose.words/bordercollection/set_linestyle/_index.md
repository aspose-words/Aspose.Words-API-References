---
title: Aspose::Words::BorderCollection::set_LineStyle method
linktitle: set_LineStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::set_LineStyle method. Sets the border style in C++.'
type: docs
weight: 22000
url: /cpp/aspose.words/bordercollection/set_linestyle/
---
## BorderCollection::set_LineStyle method


Sets the border style.

```cpp
void Aspose::Words::BorderCollection::set_LineStyle(Aspose::Words::LineStyle value)
```

## Remarks


Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.
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
