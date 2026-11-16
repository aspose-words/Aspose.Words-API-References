---
title: Aspose::Words::ControlChar::SectionBreak method
linktitle: SectionBreak
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::ControlChar::SectionBreak method. End of section character: "\x000c" or "\f". Note it has the same value as PageBreak in C++.'
type: docs
weight: 11000
url: /cpp/aspose.words/controlchar/sectionbreak/
---
## ControlChar::SectionBreak method


End of section character: "\x000c" or "\f". Note it has the same value as [PageBreak](../pagebreak/).

```cpp
static System::String & Aspose::Words::ControlChar::SectionBreak()
```

## Examples


Shows how to add various control characters to a document.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add a regular space.
builder->Write(System::String(u"Before space.") + ControlChar::SpaceChar + u"After space.");

// Add an NBSP, which is a non-breaking space.
// Unlike the regular space, this space cannot have an automatic line break at its position.
builder->Write(System::String(u"Before space.") + ControlChar::NonBreakingSpace() + u"After space.");

// Add a tab character.
builder->Write(System::String(u"Before tab.") + ControlChar::Tab() + u"After tab.");

// Add a line break.
builder->Write(System::String(u"Before line break.") + ControlChar::LineBreak() + u"After line break.");

// Add a new line and starts a new paragraph.
ASSERT_EQ(doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Paragraph, true)->get_Count(), 1);
builder->Write(System::String(u"Before line feed.") + ControlChar::LineFeed() + u"After line feed.");
ASSERT_EQ(doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Paragraph, true)->get_Count(), 2);

// The line feed character has two versions.
ASSERT_EQ(ControlChar::Lf(), ControlChar::LineFeed());

// Carriage returns and line feeds can be represented together by one character.
ASSERT_EQ(ControlChar::Cr() + ControlChar::Lf(), ControlChar::CrLf());

// Add a paragraph break, which will start a new paragraph.
builder->Write(System::String(u"Before paragraph break.") + ControlChar::ParagraphBreak() + u"After paragraph break.");
ASSERT_EQ(doc->get_FirstSection()->get_Body()->GetChildNodes(NodeType::Paragraph, true)->get_Count(), 3);

// Add a section break. This does not make a new section or paragraph.
ASSERT_EQ(doc->get_Sections()->get_Count(), 1);
builder->Write(System::String(u"Before section break.") + ControlChar::SectionBreak() + u"After section break.");
ASSERT_EQ(doc->get_Sections()->get_Count(), 1);

// Add a page break.
builder->Write(System::String(u"Before page break.") + ControlChar::PageBreak() + u"After page break.");

// A page break is the same value as a section break.
ASSERT_EQ(ControlChar::SectionBreak(), ControlChar::PageBreak());

// Insert a new section, and then set its column count to two.
doc->AppendChild<System::SharedPtr<Aspose::Words::Section>>(System::MakeObject<Aspose::Words::Section>(doc));
builder->MoveToSection(1);
builder->get_CurrentSection()->get_PageSetup()->get_TextColumns()->SetCount(2);

// We can use a control character to mark the point where text moves to the next column.
builder->Write(System::String(u"Text at end of column 1.") + ControlChar::ColumnBreak() + u"Text at beginning of column 2.");

doc->Save(get_ArtifactsDir() + u"ControlChar.InsertControlChars.docx");

// There are char and string counterparts for most characters.
ASPOSE_ASSERT_EQ(ControlChar::CellChar, System::Convert::ToChar(ControlChar::Cell()));
ASPOSE_ASSERT_EQ(ControlChar::NonBreakingSpaceChar, System::Convert::ToChar(ControlChar::NonBreakingSpace()));
ASPOSE_ASSERT_EQ(ControlChar::TabChar, System::Convert::ToChar(ControlChar::Tab()));
ASPOSE_ASSERT_EQ(ControlChar::LineBreakChar, System::Convert::ToChar(ControlChar::LineBreak()));
ASPOSE_ASSERT_EQ(ControlChar::LineFeedChar, System::Convert::ToChar(ControlChar::LineFeed()));
ASPOSE_ASSERT_EQ(ControlChar::ParagraphBreakChar, System::Convert::ToChar(ControlChar::ParagraphBreak()));
ASPOSE_ASSERT_EQ(ControlChar::SectionBreakChar, System::Convert::ToChar(ControlChar::SectionBreak()));
ASPOSE_ASSERT_EQ(ControlChar::SectionBreakChar, System::Convert::ToChar(ControlChar::PageBreak()));
ASPOSE_ASSERT_EQ(ControlChar::ColumnBreakChar, System::Convert::ToChar(ControlChar::ColumnBreak()));
```
## See Also

* Class [ControlChar](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
