---
title: SectionLayoutMode
second_title: Aspose.Words for C++ API Reference
description: Specifies the layout mode for a section allowing to define the document grid behavior.
type: docs
weight: 1483
url: /cpp/aspose.words/sectionlayoutmode/
---
## SectionLayoutMode enum


Specifies the layout mode for a section allowing to define the document grid behavior.

```cpp
enum class SectionLayoutMode
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| Default | 0 | Specifies that no document grid shall be applied to the contents of the corresponding section in the document. |
| Grid | 1 | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will not be automatically aligned with gridlines on typing. |
| LineGrid | 2 | Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page. |
| SnapToChars | 3 | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will be automatically aligned with gridlines on typing. |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words](../../)
