---
title: Aspose::Words::Border::set_DistanceFromText method
linktitle: set_DistanceFromText
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Border::set_DistanceFromText method. Sets distance of the border from text or from the page edge in points in C++.'
type: docs
weight: 16000
url: /cpp/aspose.words/border/set_distancefromtext/
---
## Border::set_DistanceFromText method


Sets distance of the border from text or from the page edge in points.

```cpp
void Aspose::Words::Border::set_DistanceFromText(double value)
```

## Remarks

 Has no effect and will be automatically reset to zero for borders of table cells. 
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

* Class [Border](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
