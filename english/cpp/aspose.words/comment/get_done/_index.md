---
title: Aspose::Words::Comment::get_Done method
linktitle: get_Done
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Comment::get_Done method. Gets or sets flag indicating that the comment has been marked done in C++.'
type: docs
weight: 8000
url: /cpp/aspose.words/comment/get_done/
---
## Comment::get_Done method


Gets or sets flag indicating that the comment has been marked done.

```cpp
bool Aspose::Words::Comment::get_Done() const
```


## Examples



Shows how to mark a comment as "done". 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Helo world!");

// Insert a comment to point out an error.
auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Fix the spelling error!");
doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

// Comments have a "Done" flag, which is set to "false" by default.
// If a comment suggests that we make a change within the document,
// we can apply the change, and then also set the "Done" flag afterwards to indicate the correction.
ASSERT_FALSE(comment->get_Done());

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_Runs()->idx_get(0)->set_Text(u"Hello world!");
comment->set_Done(true);

// Comments that are "done" will differentiate themselves
// from ones that are not "done" with a faded text color.
comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"J.D.", System::DateTime::get_Now());
comment->SetText(u"Add text to this paragraph.");
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);

doc->Save(get_ArtifactsDir() + u"Comment.Done.docx");
```

## See Also

* Class [Comment](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
