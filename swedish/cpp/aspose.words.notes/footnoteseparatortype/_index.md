---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. Anger typen av fotnot-/slutnotseparator i C++."
type: docs
weight: 6500
url: /sv/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Anger typen av fotnot-/slutnotseparator.

```cpp
enum class FootnoteSeparatorType
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| FootnoteSeparator | 0 | Separator mellan huvudtext och fotnottext. |
| FootnoteContinuationSeparator | 1 | Skrivs ut ovanför fotnottext på en sida när texten måste fortsättas från en föregående sida. |
| FootnoteContinuationNotice | 2 | Skrivs ut under fotnottext på en sida när fotnottexten måste fortsättas på en efterföljande sida. |
| EndnoteSeparator | 3 | Separator mellan huvudtext och slutnottext. |
| EndnoteContinuationSeparator | 4 | Skrivs ut ovanför slutnottext på en sida när texten måste fortsättas från en föregående sida. |
| EndnoteContinuationNotice | 5 | Skrivs ut under slutnottext på en sida när slutnottexten måste fortsättas på en efterföljande sida. |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
