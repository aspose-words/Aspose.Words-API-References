---
title: "Метод Aspose::Words::IHyphenationCallback::RequestDictionary. Уведомляет приложение, что словарь переносов для указанного языка не найден и может потребоваться его регистрация. Реализация должна найти словарь и зарегистрировать его с помощью методов RegisterDictionary(). Если словарь недоступен для указанного языка, реализация может отказаться от дальнейших вызовов для того же языка, используя RegisterDictionary() с null‑значением в C++."
linktitle: "Метод Aspose::Words::IHyphenationCallback::GetType"
second_title: "Справочник API Aspose.Words для C++"
description: "Как использовать метод GetType класса Aspose::Words::IHyphenationCallback в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback::RequestDictionary method


Уведомляет приложение, что словарь переносов для указанного языка не найден и может потребоваться его регистрация. Реализация должна найти словарь и зарегистрировать его с помощью методов [RegisterDictionary()](../). Если словарь недоступен для указанного языка, реализация может отказаться от дальнейших вызовов для того же языка, используя [RegisterDictionary()](../) со значением **null**.

```cpp
virtual void Aspose::Words::IHyphenationCallback::RequestDictionary(System::String language)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| language | System::String | Имя языка, например "en-US". См. документацию .NET по "culture name" и RFC 4646 для получения подробностей. |

## См. также

* Interface [IHyphenationCallback](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
