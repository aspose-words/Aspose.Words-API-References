---
title: Aspose::Words::PageSetup::get_BorderAlwaysInFront method
linktitle: get_BorderAlwaysInFront
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_BorderAlwaysInFront method. Specifies where the page border is positioned relative to intersecting texts and objects in C++.'
type: docs
weight: 4000
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
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(Aspose::Words::PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(Aspose::Words::BorderType::Top);
border->set_LineStyle(Aspose::Words::LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
