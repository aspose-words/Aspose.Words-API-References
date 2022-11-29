---
title: get_Color
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the border color.
type: docs
weight: 40
url: /cpp/aspose.words/bordercollection/get_color/
---
## BorderCollection::get_Color method


Gets or sets the border color.

```cpp
System::Drawing::Color Aspose::Words::BorderCollection::get_Color()
```

## Remarks


Returns the color of the first border in the collection.

Sets the color of all borders in the collection excluding diagonal borders.

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
