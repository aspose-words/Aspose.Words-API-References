---
title: "Aspose::Words::Settings::OdsoFieldMapData класс"
linktitle: "OdsoFieldMapData"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::OdsoFieldMapData class. Указывает, как столбец во внешнем источнике данных должен быть сопоставлен с предопределёнными полями слияния в документе. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 5000
url: /ru/cpp/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class


Указывает, как столбец во внешнем источнике данных будет сопоставлен с предопределёнными полями слияния в документе. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoFieldMapData : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Возвращает глубокую копию этого объекта. |
| [get_Column](./get_column/)() const | Указывает нулевой индекс столбца во внешнем источнике данных, который будет сопоставлен с локальным именем конкретного поля MERGEFIELD. Значение по умолчанию — 0. |
| [get_MappedName](./get_mappedname/)() const | Указывает имя предопределённого поля слияния, которое будет сопоставлено с номером столбца, указанным свойством [Column](./get_column/) в этом сопоставлении полей. Значение по умолчанию — пустая строка. |
| [get_Name](./get_name/)() const | Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан свойством [Column](./get_column/). Значение по умолчанию — пустая строка. |
| [get_Type](./get_type/)() const | Указывает, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. Значение по умолчанию — [Default](../odsofieldmappingtype/). |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoFieldMapData](./odsofieldmapdata/)() |  |
| [set_Column](./set_column/)(int32_t) | Указывает нулевой индекс столбца во внешнем источнике данных, который будет сопоставлен с локальным именем конкретного поля MERGEFIELD. Значение по умолчанию — 0. |
| [set_MappedName](./set_mappedname/)(const System::String\&) | Указывает имя предопределённого поля слияния, которое будет сопоставлено с номером столбца, указанным свойством [Column](./get_column/) в этом сопоставлении полей. Значение по умолчанию — пустая строка. |
| [set_Name](./set_name/)(const System::String\&) | Указывает имя столбца во внешнем источнике данных для столбца, индекс которого указан свойством [Column](./get_column/). Значение по умолчанию — пустая строка. |
| [set_Type](./set_type/)(Aspose::Words::Settings::OdsoFieldMappingType) | Указывает, сопоставлено ли данное поле слияния с колонкой во внешнем источнике данных. Значение по умолчанию — [Default](../odsofieldmappingtype/). |
| static [Type](./type/)() |  |
## Примечания


Microsoft Word предоставляет некоторые предопределённые имена полей слияния, которые можно вставлять в документ как MERGEFIELD или использовать в полях ADDRESSBLOCK или GREETINGLINE. Информация, указанная в [OdsoFieldMapData](./), позволяет сопоставить один столбец во внешнем источнике данных с отдельным предопределённым полем слияния.

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
