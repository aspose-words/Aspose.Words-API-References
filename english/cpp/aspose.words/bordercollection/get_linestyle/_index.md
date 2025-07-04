---
title: Aspose::Words::BorderCollection::get_LineStyle method
linktitle: get_LineStyle
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::get_LineStyle method. Gets or sets the border style in C++.'
type: docs
weight: 10000
url: /cpp/aspose.words/bordercollection/get_linestyle/
---
## BorderCollection::get_LineStyle method


Gets or sets the border style.

```cpp
Aspose::Words::LineStyle Aspose::Words::BorderCollection::get_LineStyle()
```

## Remarks


Returns the style of the first border in the collection.

Sets the style of all borders in the collection excluding diagonal borders.

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

* Enum [LineStyle](../../linestyle/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
