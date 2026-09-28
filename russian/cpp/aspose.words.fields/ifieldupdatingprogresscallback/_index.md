---
title: "Aspose::Words::Fields::IFieldUpdatingProgressCallback интерфейс"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::IFieldUpdatingProgressCallback интерфейс. Реализуйте этот интерфейс, если хотите отслеживать прогресс обновления полей в C++."
type: docs
weight: 124000
url: /ru/cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


Реализуйте этот интерфейс, если хотите отслеживать прогресс обновления поля.

```cpp
class IFieldUpdatingProgressCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Fields::FieldUpdatingProgressArgs\>) | Пользовательский метод, который вызывается при изменении прогресса обновления. |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
