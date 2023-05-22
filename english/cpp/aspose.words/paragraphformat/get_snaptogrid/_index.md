---
title: Aspose::Words::ParagraphFormat::get_SnapToGrid method
linktitle: get_SnapToGrid
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ParagraphFormat::get_SnapToGrid method. Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph in C++.'
type: docs
weight: 30000
url: /cpp/aspose.words/paragraphformat/get_snaptogrid/
---
## ParagraphFormat::get_SnapToGrid method


Specifies whether the current paragraph should use the document grid lines per page settings when laying out the contents in the paragraph.

```cpp
bool Aspose::Words::ParagraphFormat::get_SnapToGrid()
```


## Examples



Shows how to specify a limit for the number of lines that each page may have. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Enable pitching, and then use it to set the number of lines per page in this section.
// A large enough font size will push some lines down onto the next page to avoid overlapping characters.
builder->get_PageSetup()->set_LayoutMode(SectionLayoutMode::LineGrid);
builder->get_PageSetup()->set_LinesPerPage(15);

builder->get_ParagraphFormat()->set_SnapToGrid(true);

for (int i = 0; i < 30; i++)
{
    builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ");
}

doc->Save(ArtifactsDir + u"PageSetup.LinesPerPage.docx");
```

## See Also

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
