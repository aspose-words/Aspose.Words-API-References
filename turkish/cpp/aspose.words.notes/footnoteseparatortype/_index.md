---
title: "Aspose::Words::Notes::FootnoteSeparatorType enum"
linktitle: "FootnoteSeparatorType"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Notes::FootnoteSeparatorType enum. C++'da dipnot/sonnot ayırıcı tipini belirtir."
type: docs
weight: 6500
url: /tr/cpp/aspose.words.notes/footnoteseparatortype/
---
## FootnoteSeparatorType enum


Dipnot/sonnot ayırıcı tipini belirtir.

```cpp
enum class FootnoteSeparatorType
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| FootnoteSeparator | 0 | Ana metin ile dipnot metni arasındaki ayırıcı. |
| FootnoteContinuationSeparator | 1 | Metin önceki sayfadan devam etmesi gerektiğinde, sayfadaki dipnot metninin üzerinde yazdırılır. |
| FootnoteContinuationNotice | 2 | Dipnot metni sonraki bir sayfada devam etmesi gerektiğinde, sayfadaki dipnot metninin altında yazdırılır. |
| EndnoteSeparator | 3 | Ana metin ile sonnot metni arasındaki ayırıcı. |
| EndnoteContinuationSeparator | 4 | Metin önceki sayfadan devam etmesi gerektiğinde, sayfadaki sonnot metninin üzerinde yazdırılır. |
| EndnoteContinuationNotice | 5 | Sonnot metni sonraki bir sayfada devam etmesi gerektiğinde, sayfadaki sonnot metninin altında yazdırılır. |


## Örnekler



Sonnot ayırıcıyı nasıl kaldıracağınızı gösterir.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Footnotes and endnotes.docx");

System::SharedPtr<Aspose::Words::Notes::FootnoteSeparator> endnoteSeparator = doc->get_FootnoteSeparators()->idx_get(Aspose::Words::Notes::FootnoteSeparatorType::EndnoteSeparator);
// Sonnot ayırıcıyı kaldır.
endnoteSeparator->get_FirstParagraph()->get_FirstChild()->Remove();
```


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
