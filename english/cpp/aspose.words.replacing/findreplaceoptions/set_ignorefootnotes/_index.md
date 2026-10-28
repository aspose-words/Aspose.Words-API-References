---
title: Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreFootnotes method
linktitle: set_IgnoreFootnotes
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreFootnotes method. Sets a boolean value indicating either to ignore footnotes. The default value is false in C++.'
type: docs
weight: 26000
url: /cpp/aspose.words.replacing/findreplaceoptions/set_ignorefootnotes/
---
## FindReplaceOptions::set_IgnoreFootnotes method


Sets a boolean value indicating either to ignore footnotes. The default value is **false**.

```cpp
void Aspose::Words::Replacing::FindReplaceOptions::set_IgnoreFootnotes(bool value)
```

## Examples


Shows how to ignore footnotes during a find-and-replace operation.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
// operation to ignore text inside footnotes.
// Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
// operation to also search for text inside footnotes.
auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```
## See Also

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
