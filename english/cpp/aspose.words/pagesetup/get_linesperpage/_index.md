---
title: Aspose::Words::PageSetup::get_LinesPerPage method
linktitle: get_LinesPerPage
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_LinesPerPage method. Gets or sets the number of lines per page in the document grid in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words/pagesetup/get_linesperpage/
---
## PageSetup::get_LinesPerPage method


Gets or sets the number of lines per page in the document grid.

```cpp
int32_t Aspose::Words::PageSetup::get_LinesPerPage()
```

## Remarks


Minimum value of the property is 1. Maximum value depends on page height and font size of the Normal style. Minimum line pitch is 136 percent of the font size. For example, maximum number of lines per page of a Letter page with one-inch margins is 39.

By default, the property has a value, on which line pitch is in 1.5 times greater than font size of the Normal style.

## Examples



Shows how to specify a limit for the number of lines that each page may have. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Enable pitching, and then use it to set the number of lines per page in this section.
// A large enough font size will push some lines down onto the next page to avoid overlapping characters.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int32_t i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(get_ArtifactsDir() + u"PageSetup.LinesPerPage.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
