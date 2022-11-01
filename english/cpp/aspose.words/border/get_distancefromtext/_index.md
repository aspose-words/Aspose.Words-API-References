---
title: get_DistanceFromText
second_title: Aspose.Words for C++ API Reference
description: Gets or sets distance of the border from text or from the page edge in points.
type: docs
weight: 40
url: /cpp/aspose.words/border/get_distancefromtext/
---
## Border.get_DistanceFromText method


Gets or sets distance of the border from text or from the page edge in points.

```cpp
double Aspose::Words::Border::get_DistanceFromText()
```


## Examples




Shows how to create a wide blue band border at the top of the first page. 
```cpp
auto doc = MakeObject<Document>();

SharedPtr<PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(PageBorderAppliesTo::FirstPage);

SharedPtr<Border> border = pageSetup->get_Borders()->idx_get(BorderType::Top);
border->set_LineStyle(LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(ArtifactsDir + u"PageSetup.PageBorderProperties.docx");
```

