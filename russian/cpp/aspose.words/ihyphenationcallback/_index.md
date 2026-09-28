---
title: "Aspose::Words::IHyphenationCallback интерфейс"
linktitle: "IHyphenationCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::IHyphenationCallback интерфейс. Реализуется классами, которые могут регистрировать словари переносов в C++."
type: docs
weight: 78000
url: /ru/cpp/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface


Реализуется классами, которые могут регистрировать словари переносов.

```cpp
class IHyphenationCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [RequestDictionary](./requestdictionary/)(System::String) | Уведомляет приложение, что словарь переносов для указанного языка не найден и может потребоваться его регистрация. Реализация должна найти словарь и зарегистрировать его с помощью методов [RegisterDictionary()](../). Если словарь недоступен для указанного языка, реализация может отказаться от дальнейших вызовов для того же языка, используя [RegisterDictionary()](../) со значением **null**. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
