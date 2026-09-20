---
title: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource метод"
linktitle: "GetDataSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource метод. Движок слияния почты Aspose.Words вызывает этот метод, когда встречает начало верхнего уровня региона слияния почты в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.mailmerging/imailmergedatasourceroot/getdatasource/
---
## IMailMergeDataSourceRoot::GetDataSource method


Движок слияния почты Aspose.Words вызывает этот метод, когда встречает начало верхнего уровня области слияния почты.

```cpp
virtual System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> Aspose::Words::MailMerging::IMailMergeDataSourceRoot::GetDataSource(System::String tableName)=0
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| tableName | System::String | Имя области слияния, указанное в шаблоне документа. Без учёта регистра. |

### ReturnValue

Объект источника данных, который предоставляет доступ к записям указанной таблицы.
## Примечания


Когда движки слияния почты Aspose.Words заполняют документ данными и встречают MERGEFIELD TableStart:TableName, они вызывают [GetDataSource()](./) у этого объекта. Ваша реализация должна вернуть новый объект источника данных. Aspose.Words будет использовать возвращённый источник данных для заполнения региона слияния почты.

Если источник данных (таблица) с указанным именем не существует, ваша реализация должна вернуть **null**.

## См. также

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Interface [IMailMergeDataSourceRoot](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
