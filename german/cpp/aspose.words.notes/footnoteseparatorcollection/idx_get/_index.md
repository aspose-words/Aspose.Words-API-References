---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get Methode"
linktitle: "idx_get"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get Methode. Ruft einen FootnoteSeparator des angegebenen Typs in C++ ab."
type: docs
weight: 5000
url: /de/cpp/aspose.words.notes/footnoteseparatorcollection/idx_get/
---
## FootnoteSeparatorCollection::idx_get method


Ruft einen [FootnoteSeparator](../../footnoteseparator/) des angegebenen Typs ab.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> Aspose::Words::Notes::FootnoteSeparatorCollection::idx_get(Aspose::Words::Notes::FootnoteSeparatorType separatorType)
```


## Beispiele



Zeigt, wie das Format des Fußnotentrennzeichens verwaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Fußnotentrennzeichen ausrichten.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Siehe auch

* Class [FootnoteSeparator](../../footnoteseparator/)
* Enum [FootnoteSeparatorType](../../footnoteseparatortype/)
* Class [FootnoteSeparatorCollection](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
