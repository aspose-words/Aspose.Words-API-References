---
title: Aspose::Words::DocumentBase::get_FootnoteSeparators method
linktitle: get_FootnoteSeparators
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::DocumentBase::get_FootnoteSeparators method. Provides access to the footnote/endnote separators defined in the document in C++.'
type: docs
weight: 4500
url: /cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Provides access to the footnote/endnote separators defined in the document.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## Examples



Shows how to remove endnote separator. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Remove endnote separator.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Shows how to manage footnote separator format. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Align footnote separator.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## See Also

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
