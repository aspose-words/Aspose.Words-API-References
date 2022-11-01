---
title: get_CharactersPerLine
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the number of characters per line in the document grid.
type: docs
weight: 131
url: /cpp/aspose.words/pagesetup/get_charactersperline/
---
## PageSetup.get_CharactersPerLine method


Gets or sets the number of characters per line in the document grid.

```cpp
int32_t Aspose::Words::PageSetup::get_CharactersPerLine()
```


Minimum value of the property is 1. Maximum value depends on page width and font size of the Normal style. Minimum character pitch is 90 percent of the font size. For example, maximum number of characters per line of a Letter page with one-inch margins is 43.

By default, the property has a value, on which character pitch equals to font size of the Normal style.

## Examples




Shows how to specify a for the number of characters that each line may have. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Enable pitching, and then use it to set the number of characters per line in this section.
builder->get_PageSetup()->set_LayoutMode(SectionLayoutMode::Grid);
builder->get_PageSetup()->set_CharactersPerLine(10);

// The number of characters also depends on the size of the font.
doc->get_Styles()->idx_get(u"Normal")->get_Font()->set_Size(20);

ASSERT_EQ(8, doc->get_FirstSection()->get_PageSetup()->get_CharactersPerLine());

builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(ArtifactsDir + u"PageSetup.CharactersPerLine.docx");
```

