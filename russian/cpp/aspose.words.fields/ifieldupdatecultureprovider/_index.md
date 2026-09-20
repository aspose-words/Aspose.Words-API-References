---
title: "Интерфейс Aspose::Words::Fields::IFieldUpdateCultureProvider"
linktitle: "IFieldUpdateCultureProvider"
second_title: "Справочник API Aspose.Words для C++"
description: "Интерфейс Aspose::Words::Fields::IFieldUpdateCultureProvider. При реализации предоставляет объект CultureInfo, который следует использовать во время обновления конкретного поля в C++."
type: docs
weight: 122000
url: /ru/cpp/aspose.words.fields/ifieldupdatecultureprovider/
---
## IFieldUpdateCultureProvider interface


При реализации предоставляет объект **CultureInfo**, который следует использовать во время обновления конкретного поля.

```cpp
class IFieldUpdateCultureProvider : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [GetCulture](./getculture/)(System::String, System::SharedPtr\<Aspose::Words::Fields::Field\>) | Возвращает объект **CultureInfo**, который будет использоваться во время обновления поля. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
