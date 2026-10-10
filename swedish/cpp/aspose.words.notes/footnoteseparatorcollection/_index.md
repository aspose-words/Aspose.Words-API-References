---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection klass"
linktitle: "FootnoteSeparatorCollection"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection klass. Tillhandahåller typad åtkomst till FootnoteSeparator-noder i ett dokument i C++."
type: docs
weight: 3667
url: /sv/cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


Tillhandahåller typad åtkomst till [FootnoteSeparator](../footnoteseparator/)-noder i ett dokument.

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | Hämtar en [FootnoteSeparator](../footnoteseparator/) av den angivna typen. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Exempel



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
