---
title: PageBorderAppliesTo
second_title: Aspose.Words for C++ API Reference
description: Specifies which pages the page border is printed on.
type: docs
weight: 1366
url: /cpp/aspose.words/pageborderappliesto/
---
## PageBorderAppliesTo enum


Specifies which pages the page border is printed on.

```cpp
enum class PageBorderAppliesTo
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| AllPages | 0 | Page border is shown on all pages of the section. |
| FirstPage | 1 | Page border is shown on the first page of the section only. |
| OtherPages | 2 | Page border is shown on all pages except the first page of the section. |


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
