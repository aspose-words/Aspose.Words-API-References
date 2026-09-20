---
title: "Aspose::Words::Fields::IFieldUpdatingCallback интерфейс"
linktitle: "IFieldUpdatingCallback"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::IFieldUpdatingCallback интерфейс. Реализуйте этот интерфейс, если хотите, чтобы ваши собственные пользовательские методы вызывались во время обновления поля в C++."
type: docs
weight: 123000
url: /ru/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Реализуйте этот интерфейс, если хотите, чтобы ваши собственные пользовательские методы вызывались во время обновления поля.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Пользовательский метод, который вызывается сразу после обновления поля. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Пользовательский метод, который вызывается непосредственно перед обновлением поля. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
