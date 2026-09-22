---
title: "Aspose::Words::Notes::FootnoteSeparatorCollection class"
linktitle: "FootnoteSeparatorCollection"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteSeparatorCollection class. C++ içinde bir belgenin FootnoteSeparator düğümlerine tiplenmiş erişim sağlar."
type: docs
weight: 3667
url: /tr/cpp/aspose.words.notes/footnoteseparatorcollection/
---
## FootnoteSeparatorCollection class


Bir belgenin [FootnoteSeparator](../footnoteseparator/) düğümlerine tiplenmiş erişim sağlar.

```cpp
class FootnoteSeparatorCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator>>
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [FootnoteSeparatorCollection](./footnoteseparatorcollection/)() |  |
| [GetEnumerator](./getenumerator/)() override |  |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::Notes::FootnoteSeparatorType) | Belirtilen türde bir [FootnoteSeparator](../footnoteseparator/) getirir. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Örnekler



Dipnot ayırıcı biçimini nasıl yöneteceğinizi gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> footnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::FootnoteSeparator);
// Dipnot ayırıcıyı hizala.
footnoteSeparator->get_FirstParagraph()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
```

## Ayrıca Bakınız

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
