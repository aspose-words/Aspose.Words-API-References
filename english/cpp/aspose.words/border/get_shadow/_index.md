---
title: get_Shadow
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value indicating whether the border has a shadow.
type: docs
weight: 92
url: /cpp/aspose.words/border/get_shadow/
---
## Border.get_Shadow method


Gets or sets a value indicating whether the border has a shadow.

```cpp
bool Aspose::Words::Border::get_Shadow()
```


In Microsoft Word, for a border to have a shadow, the borders on all four sides (left, top, right and bottom) should be of the same type, width, color and all should have the Shadow property set to true.

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

