---
title: Aspose::Words::Story::get_LastParagraph method
linktitle: get_LastParagraph
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Story::get_LastParagraph method. Gets the last paragraph in the story in C++.'
type: docs
weight: 5000
url: /cpp/aspose.words/story/get_lastparagraph/
---
## Story::get_LastParagraph method


Gets the last paragraph in the story.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Story::get_LastParagraph()
```


## Examples



Shows how to move a [DocumentBuilder](../../documentbuilder/)'s cursor position to a specified node. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);
builder->Writeln(u"Run 1. ");

// The document builder has a cursor, which acts as the part of the document
// where the builder appends new nodes when we use its document construction methods.
// This cursor functions in the same way as Microsoft Word's blinking cursor,
// and it also always ends up immediately after any node that the builder just inserted.
// To append content to a different part of the document,
// we can move the cursor to a different node with the "MoveTo" method.
builder->MoveTo(doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0));

// The cursor is now in front of the node that we moved it to.
// Adding a second run will insert it in front of the first run.
builder->Writeln(u"Run 2. ");

ASSERT_EQ(u"Run 2. \rRun 1.", doc->GetText().Trim());

// Move the cursor to the end of the document to continue appending text to the end as before.
builder->MoveTo(doc->get_LastSection()->get_Body()->get_LastParagraph());
builder->Writeln(u"Run 3. ");

ASSERT_EQ(u"Run 2. \rRun 1. \rRun 3.", doc->GetText().Trim());
```

## See Also

* Class [Paragraph](../../paragraph/)
* Class [Story](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
