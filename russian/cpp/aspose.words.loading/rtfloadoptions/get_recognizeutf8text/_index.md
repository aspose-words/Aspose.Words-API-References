---
title: "Метод Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text"
linktitle: "get_RecognizeUtf8Text"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text. Когда установлен в true, будет пытаться обнаружить символы UTF8, они будут сохранены при импорте в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.loading/rtfloadoptions/get_recognizeutf8text/
---
## RtfLoadOptions::get_RecognizeUtf8Text method


Когда установлено значение **true**, будет попытка обнаружить UTF8‑символы, они будут сохранены при импорте.

```cpp
bool Aspose::Words::Loading::RtfLoadOptions::get_RecognizeUtf8Text() const
```

## Примечания


Значение по умолчанию — **false**.

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
