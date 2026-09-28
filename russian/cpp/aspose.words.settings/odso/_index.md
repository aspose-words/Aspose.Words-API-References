---
title: "Aspose::Words::Settings::Odso class"
linktitle: "Odso"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::Odso class. Указывает параметры Office Data Source Object (ODSO) для источника данных слияния писем. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.settings/odso/
---
## Odso class


Указывает настройки объекта источника данных Office (ODSO) для источника данных слияния почты. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class Odso : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clone](./clone/)() | Возвращает глубокую копию этого объекта. |
| [get_ColumnDelimiter](./get_columndelimiter/)() const | Указывает символ, который будет интерпретироваться как разделитель столбцов, используемый для разделения столбцов во внешних источниках данных. Значение по умолчанию — 0, что означает отсутствие определённого разделителя столбцов. |
| [get_DataSource](./get_datasource/)() const | Указывает расположение внешнего источника данных, который будет подключён к документу для выполнения слияния писем. Значение по умолчанию — пустая строка. |
| [get_DataSourceType](./get_datasourcetype/)() const | Указывает тип внешнего источника данных, который будет подключён в рамках информации о соединении ODSO для этого слияния писем. Значение по умолчанию — [Default](../odsodatasourcetype/). |
| [get_FieldMapDatas](./get_fieldmapdatas/)() const | Получает коллекцию объектов, которые указывают, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. Этот объект никогда не является **null**. |
| [get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/)() const | Указывает, что хост‑приложение должно рассматривать первую строку данных в указанном внешнем источнике данных как строку заголовка, содержащую имена каждого столбца в источнике данных. Значение по умолчанию — **false**. |
| [get_RecipientDatas](./get_recipientdatas/)() const | Получает коллекцию объектов, которые указывают включение/исключение отдельных записей в слиянии писем. Этот объект никогда не является **null**. |
| [get_TableName](./get_tablename/)() const | Указывает конкретный набор данных, к которому источник должен быть подключён во внешнем источнике данных. Значение по умолчанию — пустая строка. |
| [get_UdlConnectString](./get_udlconnectstring/)() const | Указывает строку подключения Universal Data Link (UDL), используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [Odso](./odso/)() |  |
| [set_ColumnDelimiter](./set_columndelimiter/)(char16_t) | Сеттер для [Aspose::Words::Settings::Odso::get_ColumnDelimiter](./get_columndelimiter/). |
| [set_DataSource](./set_datasource/)(const System::String\&) | Указывает расположение внешнего источника данных, который будет подключён к документу для выполнения слияния писем. Значение по умолчанию — пустая строка. |
| [set_DataSourceType](./set_datasourcetype/)(Aspose::Words::Settings::OdsoDataSourceType) | Сеттер для [Aspose::Words::Settings::Odso::get_DataSourceType](./get_datasourcetype/). |
| [set_FieldMapDatas](./set_fieldmapdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoFieldMapDataCollection\>\&) | Устанавливает коллекцию объектов, которые определяют, как столбцы из внешнего источника данных сопоставляются с предопределёнными именами полей слияния в документе. Этот объект никогда не является **null**. |
| [set_FirstRowContainsColumnNames](./set_firstrowcontainscolumnnames/)(bool) | Сеттер для [Aspose::Words::Settings::Odso::get_FirstRowContainsColumnNames](./get_firstrowcontainscolumnnames/). |
| [set_RecipientDatas](./set_recipientdatas/)(const System::SharedPtr\<Aspose::Words::Settings::OdsoRecipientDataCollection\>\&) | Устанавливает коллекцию объектов, которые определяют включение/исключение отдельных записей в слиянии почты. Этот объект никогда не является **null**. |
| [set_TableName](./set_tablename/)(const System::String\&) | Указывает конкретный набор данных, к которому источник должен быть подключён во внешнем источнике данных. Значение по умолчанию — пустая строка. |
| [set_UdlConnectString](./set_udlconnectstring/)(const System::String\&) | Указывает строку подключения Universal Data Link (UDL), используемую для подключения к внешнему источнику данных. Значение по умолчанию — пустая строка. |
| static [Type](./type/)() |  |
## Примечания


ODSO, по-видимому, является «новым» способом, который более новые версии Microsoft Word предпочитают использовать при указании определённых типов источников данных для документа слияния почты. ODSO, вероятно, впервые появился в Microsoft Word 2000.

Использование ODSO плохо документировано, и лучший способ узнать, как использовать свойства этого объекта, — создать документ с нужным источником данных вручную в Microsoft Word, затем открыть этот документ с помощью Aspose.Words и изучить свойства объектов [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) и [Odso](../mailmergesettings/get_odso/). Это хороший подход, если вы хотите научиться программно настраивать источник данных, например.

Обычно вам не нужно создавать объекты этого класса напрямую, потому что настройки ODSO всегда доступны через свойство [Odso](../mailmergesettings/get_odso/).

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
