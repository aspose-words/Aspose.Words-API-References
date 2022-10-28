---
title: get_BorderDistanceFrom
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.
type: docs
weight: 53
url: /cpp/aspose.words/pagesetup/get_borderdistancefrom/
---
## PageSetup.get_BorderDistanceFrom method


Gets or sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.

```cpp
Aspose::Words::PageBorderDistanceFrom Aspose::Words::PageSetup::get_BorderDistanceFrom()
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

