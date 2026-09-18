---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection class"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection class. Bietet typisierten Zugriff auf FootnoteSeparator‑Knoten eines Dokuments in C++."
type: docs
weight: 3667
url: /de/cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


Bietet typisierten Zugriff auf [FootnoteSeparator](../footnoteseparator/)‑Knoten eines Dokuments.

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | Ruft einen [FootnoteSeparator](../footnoteseparator/) des angegebenen Typs ab. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Beispiele



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
