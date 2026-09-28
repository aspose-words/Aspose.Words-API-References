---
title: "Метод Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource"
linktitle: "GetChildDataSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource. Движок слияния почты Aspose.Words вызывает этот метод, когда встречает начало вложенной области слияния в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.mailmerging/imailmergedatasource/getchilddatasource/
---
## IMailMergeDataSource::GetChildDataSource method


Движок слияния писем Aspose.Words вызывает этот метод, когда встречает начало вложенного региона слияния писем.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSource::GetChildDataSource(System::String tableName)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | System::String | Имя области слияния, указанное в шаблоне документа. Без учёта регистра. |

### ReturnValue

Объект источника данных, который предоставляет доступ к записям указанной таблицы.
## Примечания


Когда движки слияния почты Aspose.Words заполняют область слияния данными и встречают начало вложенной области слияния в виде MERGEFIELD TableStart:TableName, они вызывают [GetChildDataSource()](./) у текущего объекта источника данных. Ваша реализация должна вернуть новый объект источника данных, который предоставит доступ к дочерним записям текущей родительской записи. Aspose.Words будет использовать возвращённый источник данных для заполнения вложенной области слияния.

Ниже приведены правила, которым должна соответствовать реализация [GetChildDataSource()](./).

Если таблица, представляемая этим объектом источника данных, имеет связанную дочернюю (детальную) таблицу с указанным именем, то ваша реализация должна вернуть новый объект [IMailMergeDataSource](../), который предоставит доступ к дочерним записям текущей записи. Примером этого является связь Orders / OrderDetails. Предположим, что текущий объект [IMailMergeDataSource](../) представляет таблицу Orders и содержит текущую запись заказа. Затем Aspose.Words встречает в документе "MERGEFIELD TableStart:OrderDetails" и вызывает [GetChildDataSource()](./). Вам нужно создать и вернуть объект [IMailMergeDataSource](../), который позволит Aspose.Words получить доступ к записи OrderDetails для текущего заказа.

Если у этого объекта источника данных нет связи с таблицей с указанным именем, то вам нужно вернуть объект [IMailMergeDataSource](../), который предоставит доступ ко всем записям указанной таблицы.

Если таблица с указанным именем не существует, ваша реализация должна вернуть **null**.

## См. также

* Interface [IMailMergeDataSource](../)
* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
