---
title: "Aspose::Words::DocumentBase::get_FootnoteSeparators Methode"
linktitle: "get_FootnoteSeparators"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBase::get_FootnoteSeparators Methode. Bietet Zugriff auf die im Dokument definierten Fußnoten-/Endnoten‑Trennzeichen in C++."
type: docs
weight: 4500
url: /de/cpp/aspose.words/documentbase/get_footnoteseparators/
---
## DocumentBase::get_FootnoteSeparators method


Bietet Zugriff auf die im Dokument definierten Fußnoten-/Endnoten‑Trennzeichen.

```cpp
System::SharedPtr<Aspose::Words::Notes::FootnoteSeparatorCollection> Aspose::Words::DocumentBase::get_FootnoteSeparators() const
```


## Beispiele



Zeigt, wie man das Endnotentrennzeichen entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Endnotentrennzeichen entfernen.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


Zeigt, wie das Format des Fußnotentrennzeichens verwaltet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Fußnotentrennzeichen ausrichten.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Siehe auch

* Class [FootnoteSeparatorCollection](../../../aspose.words.notes/footnoteseparatorcollection/)
* Class [DocumentBase](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
