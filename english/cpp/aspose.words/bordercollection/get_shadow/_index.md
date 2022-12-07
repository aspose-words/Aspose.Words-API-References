---
title: get_Shadow
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value indicating whether the border has a shadow.
type: docs
weight: 157
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
auto doc = MakeObject<Document>();
SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();

pageSetup->get_Borders()->set_LineStyle(LineStyle::DoubleWave);
pageSetup->get_Borders()->set_LineWidth(2);
pageSetup->get_Borders()->set_Color(System::Drawing::Color::get_Green());
pageSetup->get_Borders()->set_DistanceFromText(24);
pageSetup->get_Borders()->set_Shadow(true);

doc->Save(ArtifactsDir + u"PageSetup.PageBorders.docx");
```

## See Also

* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
