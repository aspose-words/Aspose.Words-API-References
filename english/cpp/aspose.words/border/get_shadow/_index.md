---
title: Aspose::Words::Border::get_Shadow method
linktitle: get_Shadow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::get_Shadow method. Gets or sets a value indicating whether the border has a shadow in C++.'
type: docs
weight: 9000
url: /cpp/aspose.words/border/get_shadow/
---
## Border::get_Shadow method


Gets or sets a value indicating whether the border has a shadow.

```cpp
bool Aspose::Words::Border::get_Shadow()
```

## Remarks


In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to **true**.

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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
