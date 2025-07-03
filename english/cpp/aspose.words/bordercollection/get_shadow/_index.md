---
title: Aspose::Words::BorderCollection::get_Shadow method
linktitle: get_Shadow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::BorderCollection::get_Shadow method. Gets or sets a value indicating whether the border has a shadow in C++.'
type: docs
weight: 13000
url: /cpp/aspose.words/bordercollection/get_shadow/
---
## BorderCollection::get_Shadow method


Gets or sets a value indicating whether the border has a shadow.

```cpp
bool Aspose::Words::BorderCollection::get_Shadow()
```

## Remarks


Gets the value from the first border in the collection.

Sets the value for all borders in the collection excluding diagonal borders.

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
