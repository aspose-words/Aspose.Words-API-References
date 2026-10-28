---
title: Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreInserted method
linktitle: set_IgnoreInserted
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreInserted method. Sets a boolean value indicating either to ignore text inside insert revisions. The default value is false in C++.'
type: docs
weight: 27000
url: /cpp/aspose.words.replacing/findreplaceoptions/set_ignoreinserted/
---
## FindReplaceOptions::set_IgnoreInserted method


Sets a boolean value indicating either to ignore text inside insert revisions. The default value is **false**.

```cpp
void Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreInserted(bool value)
```

## Examples


Shows how to include or ignore text inside insert revisions during a find-and-replace operation.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Writeln(u"Hello world!");

// Start tracking revisions and insert a paragraph. That paragraph will be an insert revision.
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"Hello again!");
doc->StopTrackRevisions();

ASSERT_TRUE(doc->get_FirstSection()->get_Body()->get_Paragraphs()->idx_get(1)->get_IsInsertRevision());

// We can use a "FindReplaceOptions" object to modify the find-and-replace process.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();

// Set the "IgnoreInserted" flag to "true" to get the find-and-replace
// operation to ignore paragraphs that are insert revisions.
// Set the "IgnoreInserted" flag to "false" to get the find-and-replace
// operation to also search for text inside insert revisions.
options->set_IgnoreInserted(ignoreTextInsideInsertRevisions);

doc->get_Range()->Replace(u"Hello", u"Greetings", options);

ASSERT_EQ(ignoreTextInsideInsertRevisions ? System::String(u"Greetings world!\rHello again!") : System::String(u"Greetings world!\rGreetings again!"), doc->GetText().Trim());
```
## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
