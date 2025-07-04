---
title: Aspose::Words::InlineStory::get_StoryType method
linktitle: get_StoryType
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::InlineStory::get_StoryType method. Returns the type of the story in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words/inlinestory/get_storytype/
---
## InlineStory::get_StoryType method


Returns the type of the story.

```cpp
Aspose::Words::StoryType Aspose::Words::InlineStory::get_StoryType() override=0
```


## Examples



Shows how to insert [InlineStory](../) nodes. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, nullptr);

// Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
auto table = System::MakeObject<Aspose::Words::Tables::Table>(doc);
table->EnsureMinimum();

// We can place a table inside a footnote, which will make it appear at the referencing page's footer.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild<System::SharedPtr<Aspose::Words::Tables::Table>>(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(Aspose::Words::NodeType::Table, footnote->get_LastChild()->get_NodeType());

// An InlineStory has an "EnsureMinimum()" method as well, but in this case,
// it makes sure the last child of the node is a paragraph,
// for us to be able to click and write text easily in Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Edit the appearance of the anchor, which is the small superscript number
// in the main text that points to the footnote.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// All inline story nodes have their respective story types.
ASSERT_EQ(Aspose::Words::StoryType::Footnotes, footnote->get_StoryType());

// A comment is another type of inline story.
auto comment = System::ExplicitCast<Aspose::Words::Comment>(builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// The parent paragraph of an inline story node will be the one from the main document body.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// However, the last paragraph is the one from the comment text contents,
// which will be outside the main document body in a speech bubble.
// A comment will not have any child nodes by default,
// so we can apply the EnsureMinimum() method to place a paragraph here as well.
ASSERT_TRUE(System::TestTools::IsNull(comment->get_LastParagraph()));
comment->EnsureMinimum();
ASSERT_EQ(Aspose::Words::NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Once we have a paragraph, we can move the builder to do it and write our comment.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(Aspose::Words::StoryType::Comments, comment->get_StoryType());

doc->Save(get_ArtifactsDir() + u"InlineStory.InsertInlineStoryNodes.docx");
```

## See Also

* Enum [StoryType](../../storytype/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
