---
title: get_Borders
second_title: Aspose.Words for C++ API Reference
description: Gets a collection of the page borders.
type: docs
weight: 66
url: /cpp/aspose.words/pagesetup/get_borders/
---
## PageSetup.get_Borders method


Gets a collection of the page borders.

```cpp
System::SharedPtr<Aspose::Words::BorderCollection> Aspose::Words::PageSetup::get_Borders()
```


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

