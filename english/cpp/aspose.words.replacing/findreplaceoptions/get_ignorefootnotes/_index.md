---
title: get_IgnoreFootnotes
second_title: Aspose.Words for C++ API Reference
description: Gets or sets a boolean value indicating either to ignore footnotes. The default value is false.
type: docs
weight: 105
url: /cpp/aspose.words.replacing/findreplaceoptions/get_ignorefootnotes/
---
## FindReplaceOptions.get_IgnoreFootnotes method


Gets or sets a boolean value indicating either to ignore footnotes. The default value is **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreFootnotes() const
```


## Examples




Shows how to ignore footnotes during a find-and-replace operation. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(FootnoteType::Footnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder->InsertParagraph();

builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder->InsertFootnote(FootnoteType::Endnote, u"Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Set the "IgnoreFootnotes" flag to "true" to get the find-and-replace
// operation to ignore text inside footnotes.
// Set the "IgnoreFootnotes" flag to "false" to get the find-and-replace
// operation to also search for text inside footnotes.
auto options = MakeObject<FindReplaceOptions>();
options->set_IgnoreFootnotes(isIgnoreFootnotes);
doc->get_Range()->Replace(u"Lorem ipsum", u"Replaced Lorem ipsum", options);
```

