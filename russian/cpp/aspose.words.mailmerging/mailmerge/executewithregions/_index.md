---
title: "Метод Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions"
linktitle: "ExecuteWithRegions"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions. Выполняет слияние почты из пользовательского источника данных с регионами слияния в C++."
type: docs
weight: 4000
url: /ru/cpp/aspose.words.mailmerging/mailmerge/executewithregions/
---
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\&) method


Выполняет слияние почты из пользовательского источника данных с регионами слияния почты.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSource> &dataSource)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSource | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSource\>\& | Объект, реализующий пользовательский интерфейс источника данных для слияния почты. |
## Примечания


Используйте этот метод для заполнения полей слияния почты в документе значениями из любого пользовательского источника данных, например XML‑файла или коллекций бизнес‑объектов. Вам необходимо написать свой класс, реализующий интерфейс [IMailMergeDataSource](../../imailmergedatasource/).

Вы можете использовать этот метод только когда [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) имеет значение **false**, то есть вам не требуется поддержка языков с письмом справа налево (например, арабского или иврита).

## См. также

* Interface [IMailMergeDataSource](../../imailmergedatasource/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
## MailMerge::ExecuteWithRegions(const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\&) method


Выполняет слияние почты из пользовательского источника данных с регионами слияния почты.

```cpp
void Aspose::Words::MailMerging::MailMerge::ExecuteWithRegions(const System::SharedPtr<Aspose::Words::MailMerging::IMailMergeDataSourceRoot> &dataSourceRoot)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| dataSourceRoot | const System::SharedPtr\<Aspose::Words::MailMerging::IMailMergeDataSourceRoot\>\& | Объект, реализующий пользовательский интерфейс корня источника данных слияния почты. |
## Примечания


Используйте этот метод для заполнения полей слияния почты в документе значениями из любого пользовательского источника данных, например XML‑файла или коллекций бизнес‑объектов. Вам необходимо написать свои классы, реализующие интерфейсы [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/) и [IMailMergeDataSource](../../imailmergedatasource/).

Вы можете использовать этот метод только когда [IsBidiTextSupportedOnUpdate](../../../aspose.words.fields/fieldoptions/get_isbiditextsupportedonupdate/) имеет значение **false**, то есть вам не требуется поддержка языков с письмом справа налево (например, арабского или иврита).

## См. также

* Interface [IMailMergeDataSourceRoot](../../imailmergedatasourceroot/)
* Class [MailMerge](../)
* Namespace [Aspose::Words::MailMerging](../../)
* Library [Aspose.Words for C++](../../../)
