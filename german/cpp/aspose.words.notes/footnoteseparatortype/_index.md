---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. Gibt den Typ des Fußnoten-/Endnoten-Trennzeichens in C++ an."
type: docs
weight: 6500
url: /de/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Gibt den Typ des Fußnoten/Endnoten‑Trenners an.

```cpp
enum class FootnoteSeparatorType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FootnoteSeparator | 0 | Trennzeichen zwischen Haupttext und Fußnotentext. |
| FootnoteContinuationSeparator | 1 | Wird über dem Fußnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss. |
| FootnoteContinuationNotice | 2 | Wird unter dem Fußnotentext auf einer Seite gedruckt, wenn der Fußnotentext auf einer nachfolgenden Seite fortgesetzt werden muss. |
| EndnoteSeparator | 3 | Trennzeichen zwischen Haupttext und Endnotentext. |
| EndnoteContinuationSeparator | 4 | Wird über dem Endnotentext auf einer Seite gedruckt, wenn der Text von einer vorherigen Seite fortgesetzt werden muss. |
| EndnoteContinuationNotice | 5 | Wird unter dem Endnotentext auf einer Seite gedruckt, wenn der Endnotentext auf einer nachfolgenden Seite fortgesetzt werden muss. |


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
