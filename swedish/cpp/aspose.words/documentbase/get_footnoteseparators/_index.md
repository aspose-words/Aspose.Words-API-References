---
title: "Aspose::Words::DocumentBase::get_FootnoteSeparators metod"
linktitle: "get_FootnoteSeparators"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::DocumentBase::get_FootnoteSeparators metod. Ger åtkomst till fotnot-/slutnotseparatorerna som definierats i dokumentet i C++."
type: docs
weight: 4500
url: /sv/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Tillhandahåller åtkomst till fotnot-/slutnotseparatorerna som definierats i dokumentet.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## Exempel



Visar hur man tar bort slutnotavgränsare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Ta bort slutnotavgränsare.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Visar hur man hanterar formatet för fotnotsavgränsare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Justera fotnotsavgränsare.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Se även

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
