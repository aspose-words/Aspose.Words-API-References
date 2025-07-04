---
title: Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat method
linktitle: get_IncludeTextboxesFootnotesEndnotesInStat
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat method. Specifies whether to include textboxes, footnotes and endnotes in word count statistics in C++.'
type: docs
weight: 33000
url: /cpp/aspose.words/document/get_includetextboxesfootnotesendnotesinstat/
---
## Document::get_IncludeTextboxesFootnotesEndnotesInStat method


Specifies whether to include textboxes, footnotes and endnotes in word count statistics.

```cpp
bool Aspose::Words::Document::get_IncludeTextboxesFootnotesEndnotesInStat()
```


## Examples



Shows how to include or exclude textboxes, footnotes and endnotes from word count statistics. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Writeln(u"Lorem ipsum");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"sit amet");

// By default option is set to 'false'.
doc->UpdateWordCount();
// Words count without textboxes, footnotes and endnotes.
ASSERT_EQ(2, doc->get_BuiltInDocumentProperties()->get_Words());

doc->set_IncludeTextboxesFootnotesEndnotesInStat(true);
doc->UpdateWordCount();
// Words count with textboxes, footnotes and endnotes.
ASSERT_EQ(4, doc->get_BuiltInDocumentProperties()->get_Words());
```

## See Also

* Class [Document](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
