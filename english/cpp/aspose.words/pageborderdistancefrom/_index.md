---
title: PageBorderDistanceFrom
second_title: Aspose.Words for C++ API Reference
description: Specifies the positioning of the page border relative to the page margin.
type: docs
weight: 1392
url: /cpp/aspose.words/pageborderdistancefrom/
---
## PageBorderDistanceFrom enum


Specifies the positioning of the page border relative to the page margin.

```cpp
enum class PageBorderDistanceFrom
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Text | 0 | [Border](../border/) position is measured from the page margin. |
| PageEdge | 1 | [Border](../border/) position is measured from the page edge. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
