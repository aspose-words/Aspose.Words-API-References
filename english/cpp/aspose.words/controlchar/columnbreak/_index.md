---
title: ColumnBreak
second_title: Aspose.Words for C++ API Reference
description: 'End of column character: "\x000e".'
type: docs
weight: 14
url: /cpp/aspose.words/controlchar/columnbreak/
---
## ControlChar::ColumnBreak method


End of column character: "\x000e".

```cpp
static System::String & Aspose::Words::ControlChar::ColumnBreak()
```


## Examples



Shows how to add various control characters to a document. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add a regular space.
builder->Write(String(u"Before space.") + ControlChar::SpaceChar + u"After space.");

// Add an NBSP, which is a non-breaking space.
// Unlike the regular space, this space cannot have an automatic line break at its position.
builder->Write(String(u"Before space.") + ControlChar::NonBreakingSpace() + u"After space.");

// Add a tab character.
builder->Write(String(u"Before tab.") + ControlChar::Tab() + u"After tab.");

// Add a line break.
builder->Write(String(u"Before line break.") + ControlChar::LineBreak() + u"After line break.");

// Add a new line and starts a new paragraph.
ASSERT_EQ(1, doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Paragraph, true)->get_Count());
builder->Write(String(u"Before line feed.") + ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(2, doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Paragraph, true)->get_Count());

// The line feed character has two versions.
ASSERT_EQ(ControlChar::LineFeed(), ControlChar::Lf());

// Carriage returns and line feeds can be represented together by one character.
ASSERT_EQ(ControlChar::CrLf(), ControlChar::Cr() + ControlChar::Lf());

// Add a paragraph break, which will start a new paragraph.
builder->Write(String(u"Before paragraph break.") + ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(3, doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Paragraph, true)->get_Count());

// Add a section break. This does not make a new section or paragraph.
ASSERT_EQ(1, doc->get_Sections()->get_Count());
builder->Write(String(u"Before section break.") + ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(1, doc->get_Sections()->get_Count());

// Add a page break.
builder->Write(String(u"Before page break.") + ControlChar::PageBreak() + u"After page break.");

// A page break is the same value as a section break.
ASSERT_EQ(ControlChar::PageBreak(), ControlChar::SectionBreak());

// Insert a new section, and then set its column count to two.
doc->AppendChild(MakeObject<Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// We can use a control character to mark the point where text moves to the next column.
builder->Write(String(u"Text at end of column 1.") + ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(ArtifactsDir + u"ControlChar.InsertControlChars.docx");

// There are char and string counterparts for most characters.
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::Cell()), ControlChar::CellChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::NonBreakingSpace()), ControlChar::NonBreakingSpaceChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::Tab()), ControlChar::TabChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::LineBreak()), ControlChar::LineBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::LineFeed()), ControlChar::LineFeedChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::ParagraphBreak()), ControlChar::ParagraphBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::SectionBreak()), ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::PageBreak()), ControlChar::SectionBreakChar);
ASPOSE_ASSERT_EQ(System::Convert::ToChar(ControlChar::ColumnBreak()), ControlChar::ColumnBreakChar);
```

## See Also

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
