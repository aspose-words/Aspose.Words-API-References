---
title: "Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions конструктор"
linktitle: "RtfLoadOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Конструктор Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions. Инициализирует новый экземпляр этого класса со значениями по умолчанию в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.loading/rtfloadoptions/rtfloadoptions/
---
## RtfLoadOptions::RtfLoadOptions constructor


Инициализирует новый экземпляр этого класса со значениями по умолчанию.

```cpp
Aspose::Words::Loading::RtfLoadOptions::RtfLoadOptions()
```


## Примеры



Показывает, как обнаруживать UTF-8‑символы при загрузке RTF‑документа.
```cpp
// Создайте объект "RtfLoadOptions", чтобы изменить способ загрузки RTF‑документа.
auto loadOptions = System::MakeObject<Aspose::Words::Loading::RtfLoadOptions>();

// Установите свойство "RecognizeUtf8Text" в значение "false", чтобы предположить, что документ использует кодировку ISO 8859-1
// и загружает каждый символ в документе.
// Установите свойство "RecognizeUtf8Text" в значение "true", чтобы разбирать любые переменно‑длинные символы, которые могут встречаться в тексте.
loadOptions->set_RecognizeUtf8Text(recognizeUtf8Text);

auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"UTF-8 characters.rtf", loadOptions);

ASSERT_EQ(recognizeUtf8Text ? System::String(u"“John Doe´s list of currency symbols”™\r") + u"€, ¢, £, ¥, ¤" : System::String(u"â€œJohn DoeÂ´s list of currency symbolsâ€\u009dâ„¢\r") + u"â‚¬, Â¢, Â£, Â¥, Â¤", doc->get_FirstSection()->get_Body()->GetText().Trim());
```

## См. также

* Class [RtfLoadOptions](../)
* Namespace [Aspose::Words::Loading](../../)
* Library [Aspose.Words for C++](../../../)
