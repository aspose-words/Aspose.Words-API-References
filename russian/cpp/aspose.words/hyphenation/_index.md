---
title: "Класс Aspose::Words::Hyphenation"
linktitle: "Переносы"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::Hyphenation. Предоставляет методы для работы со словарями переносов. Эти словари определяют, где слова конкретного языка могут быть перенесены. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 33000
url: /ru/cpp/aspose.words/hyphenation/
---
## Hyphenation class


Предоставляет методы для работы с словарями переносов. Эти словари определяют, где слова конкретного языка могут быть перенесены. Чтобы узнать больше, посетите статью документации [Working with Hyphenation](https://docs.aspose.com/words/cpp/working-with-hyphenation/).

```cpp
class Hyphenation
```

## Методы

| Метод | Описание |
| --- | --- |
| static [get_Callback](./get_callback/)() | Получает интерфейс обратного вызова, используемый для запроса словарей при построении разметки страниц документа. Это позволяет отложенно загружать словари, что может быть полезно при обработке документов на многих языках. |
| static [get_WarningCallback](./get_warningcallback/)() | Вызывается при загрузке шаблонов переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| [Hyphenation](./hyphenation/)() |  |
| static [IsDictionaryRegistered](./isdictionaryregistered/)(const System::String\&) | Возвращает **false**, если для указанного языка не зарегистрирован словарь или зарегистрирован Null‑словарь, **true** в противном случае. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::SharedPtr\<System::IO::Stream\>\&) | Регистрирует и загружает словарь переносов для указанного языка из потока. Выбрасывает исключение, если словарь нельзя прочитать или он имеет неверный формат. |
| static [RegisterDictionary](./registerdictionary/)(const System::String\&, const System::String\&) | Регистрирует и загружает словарь переносов для указанного языка из файла. Выбрасывает исключение, если словарь нельзя прочитать или он имеет неверный формат. Этот метод также можно использовать для регистрации Null‑словаря, чтобы предотвратить повторные вызовы [Callback](./get_callback/) для того же языка. |
| static [RegisterDictionary](./registerdictionary/)(System::String, std::basic_istream\<CharType, Traits\>\&) |  |
| static [set_Callback](./set_callback/)(const System::SharedPtr\<Aspose::Words::IHyphenationCallback\>\&) | Устанавливает интерфейс обратного вызова, используемый для запроса словарей при построении разметки страниц документа. Это позволяет отложенно загружать словари, что может быть полезно при обработке документов на многих языках. |
| static [set_WarningCallback](./set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | Вызывается при загрузке шаблонов переносов, когда обнаруживается проблема, которая может привести к потере точности форматирования. |
| static [UnregisterDictionary](./unregisterdictionary/)(const System::String\&) | Снимает регистрацию словаря переносов для указанного языка. Это отличается от регистрации Null‑словаря. Снятие регистрации словаря включает возможность обратного вызова для указанного языка. |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
