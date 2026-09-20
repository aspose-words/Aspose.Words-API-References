---
title: "Интерфейс Aspose::Words::Replacing::IReplacingCallback"
linktitle: "IReplacingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Replacing::IReplacingCallback. Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый во время операции поиска и замены в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Реализуйте этот интерфейс, если хотите иметь собственный пользовательский метод, вызываемый во время операции поиска и замены.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | Пользовательский метод, вызываемый во время операции замены для каждого найденного совпадения непосредственно перед выполнением замены. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
