---
title: "Метод Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture"
linktitle: "GetCulture"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture. Возвращает объект CultureInfo, который будет использоваться во время обновления поля в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.fields/ifieldupdatecultureprovider/getculture/
---
## IFieldUpdateCultureProvider::GetCulture method


Возвращает объект **CultureInfo**, который будет использоваться во время обновления поля.

```cpp
virtual System::SharedPtr<System::Globalization::CultureInfo> Aspose::Words::Fields::IFieldUpdateCultureProvider::GetCulture(System::String culture, System::SharedPtr<Aspose::Words::Fields::Field> field)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| культура | System::String | Имя культуры, запрашиваемой для обновляемого поля. |
| поле | System::SharedPtr\\<Aspose::Words::Fields::Field\\> | Поле, которое обновляется. |

### ReturnValue

Объект культуры, который должен использоваться при обновлении поля.

## См. также

* Class [Field](../../field/)
* Interface [IFieldUpdateCultureProvider](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
