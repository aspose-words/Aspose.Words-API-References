---
title: get_BorderAlwaysInFront
second_title: Aspose.Words for C++ API Reference
description: Specifies where the page border is positioned relative to intersecting texts and objects.
type: docs
weight: 40
url: /cpp/aspose.words/pagesetup/get_borderalwaysinfront/
---
## PageSetup::get_BorderAlwaysInFront method


Specifies where the page border is positioned relative to intersecting texts and objects.

```cpp
bool Aspose::Words::PageSetup::get_BorderAlwaysInFront()
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

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
