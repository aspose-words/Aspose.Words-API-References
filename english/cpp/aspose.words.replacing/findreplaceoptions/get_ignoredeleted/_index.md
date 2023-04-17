---
title: Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted method
linktitle: get_IgnoreDeleted
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted method. Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is false in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.replacing/findreplaceoptions/get_ignoredeleted/
---
## FindReplaceOptions::get_IgnoreDeleted method


Gets or sets a boolean value indicating either to ignore text inside delete revisions. The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreDeleted() const
```


## Examples



Shows how to include or ignore text inside delete revisions during a find-and-replace operation. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");
builder->Writeln(u"Hello again!");

// Start tracking revisions and remove the second paragraph, which will create a delete revision.
// That paragraph will persist in the document until we accept the delete revision.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->Remove();
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsDeleteRevision());

// We can use a "FindReplaceOptions" object to modify the find and replace process.
auto options = MakeObject<FindReplaceOptions>();

// Set the "IgnoreDeleted" flag to "true" to get the find-and-replace
// operation to ignore paragraphs that are delete revisions.
// Set the "IgnoreDeleted" flag to "false" to get the find-and-replace
// operation to also search for text inside delete revisions.
options->set_IgnoreDeleted(ignoreTextInsideDeleteRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideDeleteRevisions ? String(u"Greetings world!\rHello again!") : String(u"Greetings world!\rGreetings again!"),
          doc->GetText().Trim());
```

## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
