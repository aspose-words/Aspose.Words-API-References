---
title: get_StoryType
second_title: Aspose.Words for C++ API Reference
description: Returns Footnotes or Endnotes.
type: docs
weight: 92
url: /cpp/aspose.words.notes/footnote/get_storytype/
---
## Footnote::get_StoryType method


Returns [Footnotes](../../../aspose.words/storytype/) or [Endnotes](../../../aspose.words/storytype/).

```cpp
Aspose::Words::StoryType Aspose::Words::Notes::Footnote::get_StoryType() override
```


## Examples



Shows how to insert [InlineStory](../../../aspose.words/inlinestory/) nodes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
SharedPtr<Footnote> footnote = builder->InsertFootnote(FootnoteType::Footnote, nullptr);

// Table nodes have an "EnsureMinimum()" method that makes sure the table has at least one cell.
auto table = MakeObject<Table>(doc);
table->EnsureMinimum();

// We can place a table inside a footnote, which will make it appear at the referencing page's footer.
ASSERT_EQ(0, footnote->get_Tables()->get_Count());
footnote->AppendChild(table);
ASSERT_EQ(1, footnote->get_Tables()->get_Count());
ASSERT_EQ(NodeType::Table, footnote->get_LastChild()->get_NodeType());

// An InlineStory has an "EnsureMinimum()" method as well, but in this case,
// it makes sure the last child of the node is a paragraph,
// for us to be able to click and write text easily in Microsoft Word.
footnote->EnsureMinimum();
ASSERT_EQ(NodeType::Paragraph, footnote->get_LastChild()->get_NodeType());

// Edit the appearance of the anchor, which is the small superscript number
// in the main text that points to the footnote.
footnote->get_Font()->set_Name(u"Arial");
footnote->get_Font()->set_Color(System::Drawing::Color::get_Green());

// All inline story nodes have their respective story types.
ASSERT_EQ(StoryType::Footnotes, footnote->get_StoryType());

// A comment is another type of inline story.
auto comment = System::DynamicCast<Comment>(
    builder->get_CurrentParagraph()->AppendChild(MakeObject<Comment>(doc, u"John Doe", u"J. D.", System::DateTime::get_Now())));

// The parent paragraph of an inline story node will be the one from the main document body.
ASPOSE_ASSERT_EQ(doc->get_FirstSection()->get_Body()->get_FirstParagraph(), comment->get_ParentParagraph());

// However, the last paragraph is the one from the comment text contents,
// which will be outside the main document body in a speech bubble.
// A comment will not have any child nodes by default,
// so we can apply the EnsureMinimum() method to place a paragraph here as well.
ASSERT_TRUE(comment->get_LastParagraph() == nullptr);
comment->EnsureMinimum();
ASSERT_EQ(NodeType::Paragraph, comment->get_LastChild()->get_NodeType());

// Once we have a paragraph, we can move the builder to do it and write our comment.
builder->MoveTo(comment->get_LastParagraph());
builder->Write(u"My comment.");

ASSERT_EQ(StoryType::Comments, comment->get_StoryType());

doc->Save(ArtifactsDir + u"InlineStory.InsertInlineStoryNodes.docx");
```

## See Also

* Enum [StoryType](../../../aspose.words/storytype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words](../../../)
