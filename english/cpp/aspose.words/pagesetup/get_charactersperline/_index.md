---
title: Aspose::Words::PageSetup::get_CharactersPerLine method
linktitle: get_CharactersPerLine
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::PageSetup::get_CharactersPerLine method. Gets or sets the number of characters per line in the document grid in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup::get_CharactersPerLine method


Gets or sets the number of characters per line in the document grid.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```

## Remarks


Minimum value of the property is 1. Maximum value depends on page width and font size of the Normal style. Minimum character pitch is 90 percent of the font size. For example, maximum number of characters per line of a Letter page with one-inch margins is 43.

By default, the property has a value, on which character pitch equals to font size of the Normal style.

## Examples



Shows how to specify a for the number of characters that each line may have. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Enable pitching, and then use it to set the number of characters per line in this section.
builder->get_PageSetup()->set_LayoutMode(Aspose::Words::SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// The number of characters also depends on the size of the font.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CharactersPerLine.docx");
```

## See Also

* Class [PageSetup](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
