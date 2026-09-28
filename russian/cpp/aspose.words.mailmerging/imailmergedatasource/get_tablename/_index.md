---
title: "Метод Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName"
linktitle: "get_TableName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName. Возвращает имя источника данных в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words.mailmerging/imailmergedatasource/get_tablename/
---
## IMailMergeDataSource::get_TableName method


Возвращает имя источника данных.

```cpp
virtual System::String Aspose::Words::MailMerging::IMailMergeDataSource::get_TableName()=0
```


### ReturnValue

Имя источника данных. Пустая строка, если у источника данных нет имени.
## Примечания


Если вы реализуете [IMailMergeDataSource](../), верните имя источника данных из этого свойства.

Aspose.Words использует это имя для сопоставления с именем области слияния, указанным в шаблоне документа. Сравнение имени источника данных и имени области слияния не чувствительно к регистру.

## См. также

* Interface [IMailMergeDataSource](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
