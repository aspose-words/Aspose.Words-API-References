---
title: Aspose::Words::Notes::Footnote::Footnote constructor
linktitle: Footnote
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Notes::Footnote::Footnote constructor. Initializes an instance of the Footnote class in C++.'
type: docs
weight: 2000
url: /cpp/aspose.words.notes/footnote/footnote/
---
## Footnote::Footnote constructor


Initializes an instance of the [Footnote](../) class.

```cpp
Aspose::Words::Notes::Footnote::Footnote(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Notes::FootnoteType footnoteType)
```


| Parameter | Type | Description |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | The owner document. |
| footnoteType | Aspose::Words::Notes::FootnoteType | A [FootnoteType](../get_footnotetype/) value that specifies whether this is a footnote or endnote. |
## Remarks


When [Footnote](../) is created, it belongs to the specified document, but is not yet part of the document and [ParentNode](../../../aspose.words/node/get_parentnode/) is **null**.

To append [Footnote](../) to the document use[InsertAfter1()</see> or <see cref="Aspose::Words::CompositeNode::InsertBefore</tt>1(System::SharedPtr<<tt>0\>, System::SharedPtr\<Aspose::Words::Node\>)">InsertBefore1()](../) on the paragraph where you want the footnote inserted.

## Examples



Shows how to insert and customize footnotes. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add text, and reference it with a footnote. This footnote will place a small superscript reference
// mark after the text that it references and create an entry below the main body text at the bottom of the page.
// This entry will contain the footnote's reference mark and the reference text,
// which we will pass to the document builder's "InsertFootnote" method.
builder->Write(u"Main body text.");
SharedPtr<Footnote> footnote = builder->InsertFootnote(FootnoteType::Footnote, u"Footnote text.");

// If this property is set to "true", then our footnote's reference mark
// will be its index among all the section's footnotes.
// This is the first footnote, so the reference mark will be "1".
ASSERT_TRUE(footnote->get_IsAuto());

// We can move the document builder inside the footnote to edit its reference text.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(FootnoteType::Footnote, u"Footnote text.");

// We can set a custom reference mark which the footnote will use instead of its index number.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// A bookmark with the "IsAuto" flag set to true will still show its real index
// even if previous bookmarks display custom reference marks, so this bookmark's reference mark will be a "3".
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(ArtifactsDir + u"InlineStory.AddFootnote.docx");
```

## See Also

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [FootnoteType](../../footnotetype/)
* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
