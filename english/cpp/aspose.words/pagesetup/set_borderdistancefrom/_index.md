---
title: Aspose::Words::PageSetup::set_BorderDistanceFrom method
linktitle: set_BorderDistanceFrom
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::set_BorderDistanceFrom method. Sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds in C++.'
type: docs
weight: 53000
url: /cpp/aspose.words/pagesetup/set_borderdistancefrom/
---
## PageSetup::set_BorderDistanceFrom method


Sets a value that indicates whether the specified page border is measured from the edge of the page or from the text it surrounds.

```cpp
void Aspose::Words::PageSetup::set_BorderDistanceFrom(Aspose::Words::PageBorderDistanceFrom value)
```

## Examples


Shows how to create a wide blue band border at the top of the first page.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

System::SharedPtr<Aspose::Words::PageSetup> pageSetup = doc->get_Sections()->idx_get(0)->get_PageSetup();
pageSetup->set_BorderAlwaysInFront(false);
pageSetup->set_BorderDistanceFrom(PageBorderDistanceFrom::PageEdge);
pageSetup->set_BorderAppliesTo(PageBorderAppliesTo::FirstPage);

System::SharedPtr<Aspose::Words::Border> border = pageSetup->get_Borders()->idx_get(BorderType::Top);
border->set_LineStyle(LineStyle::Single);
border->set_LineWidth(30);
border->set_Color(System::Drawing::Color::get_Blue());
border->set_DistanceFromText(0);

doc->Save(get_ArtifactsDir() + u"PageSetup.PageBorderProperties.docx");
```
## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
