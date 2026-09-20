---
title: "Aspose::Words::Settings::OdsoRecipientData класс"
linktitle: "OdsoRecipientData"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::OdsoRecipientData класс. Представляет информацию об отдельной записи во внешнем источнике данных, которая должна быть исключена из слияния почты. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class


Представляет информацию об отдельной записи во внешнем источнике данных, которая должна быть исключена из слияния почты. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class OdsoRecipientData : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Возвращает глубокую копию этого объекта. |
| [get_Active](./get_active/)() const | Указывает, будет ли запись из источника данных импортирована в документ при выполнении слияния почты. Значение по умолчанию — **true**. |
| [get_Column](./get_column/)() const | Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. Значение по умолчанию — 0. |
| [get_Hash](./get_hash/)() const | Представляет хеш‑код этой записи. Иногда Microsoft Word использует [Hash](./get_hash/) всей записи вместо значения [UniqueTag](./get_uniquetag/). Значение по умолчанию — 0. |
| [get_UniqueTag](./get_uniquetag/)() const | Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию — **null**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [OdsoRecipientData](./odsorecipientdata/)() |  |
| [set_Active](./set_active/)(bool) | Указывает, будет ли запись из источника данных импортирована в документ при выполнении слияния почты. Значение по умолчанию — **true**. |
| [set_Column](./set_column/)(int32_t) | Указывает столбец в источнике данных, содержащий уникальные данные для текущей записи. Значение по умолчанию — 0. |
| [set_Hash](./set_hash/)(int32_t) | Представляет хеш‑код этой записи. Иногда Microsoft Word использует [Hash](./get_hash/) всей записи вместо значения [UniqueTag](./get_uniquetag/). Значение по умолчанию — 0. |
| [set_UniqueTag](./set_uniquetag/)(const System::ArrayPtr\<uint8_t\>\&) | Указывает содержимое данной записи в столбце, содержащем уникальные данные. Значение по умолчанию — **null**. |
| static [Type](./type/)() |  |
## Примечания


Если запись должна быть объединена в объединённый документ, то информация об этой записи не требуется. Однако если данная запись не должна быть объединена в объединённый документ, то значение уникального ключа для этой записи должно быть сохранено в свойстве [UniqueTag](./get_uniquetag/) этого объекта, чтобы указать на исключение.
## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
