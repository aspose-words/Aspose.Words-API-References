---
title: "Aspose::Words::Settings::MailMergeSettings класс"
linktitle: "MailMergeSettings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Settings::MailMergeSettings класс. Указывает всю информацию слияния почты для документа. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words.settings/mailmergesettings/
---
## MailMergeSettings class


Указывает всю информацию о слиянии почты для документа. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class MailMergeSettings : public System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| [Clear](./clear/)() | Очищает настройки слияния почты таким образом, что при сохранении документа настройки слияния почты не сохраняются, и документ становится обычным. |
| [Clone](./clone/)() | Возвращает глубокую копию этого объекта. |
| [get_ActiveRecord](./get_activerecord/)() const | Указывает индекс записи из источника данных, начинающийся с 1, который будет отображаться в Microsoft Word. Значение по умолчанию — 1. |
| [get_AddressFieldName](./get_addressfieldname/)() const | Указывает столбец в источнике данных, содержащий адреса электронной почты. Значение по умолчанию — пустая строка. |
| [get_CheckErrors](./get_checkerrors/)() const | Указывает тип отчётности об ошибках, который будет выполнять Microsoft Word при выполнении слияния почты. Значение по умолчанию — [Default](../mailmergecheckerrors/). |
| [get_ConnectString](./get_connectstring/)() const | Указывает строку подключения, используемую для соединения с внешним источником данных. Значение по умолчанию — пустая строка. |
| [get_DataSource](./get_datasource/)() const | Указывает путь к источнику данных слияния почты. Значение по умолчанию — пустая строка. |
| [get_DataType](./get_datatype/)() const | Указывает тип источника данных слияния почты и метод доступа к данным. Значение по умолчанию — [Default](../mailmergedatatype/). |
| [get_Destination](./get_destination/)() const | Указывает, как Microsoft Word будет выводить результаты слияния почты. Значение по умолчанию — [Default](../mailmergedestination/). |
| [get_DoNotSupressBlankLines](./get_donotsupressblanklines/)() const | Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединённых документах, полученных в результате слияния. Значение по умолчанию — **false**. |
| [get_HeaderSource](./get_headersource/)() const | Указывает путь к источнику заголовка слияния почты. Значение по умолчанию — пустая строка. |
| [get_LinkToQuery](./get_linktoquery/)() const | Не уверен в этом. Справочник автоматизации Microsoft Word предполагает, что это указывает, что запрос выполняется каждый раз при открытии документа в Microsoft Word. Но спецификация OOXML указывает, что это означает, что запрос содержит ссылку на внешний файл запроса, содержащий фактический запрос. Значение по умолчанию — **false**. |
| [get_MailAsAttachment](./get_mailasattachment/)() const | Указывает, что документы, создаваемые во время операции слияния почты, должны отправляться по электронной почте в виде вложения, а не в теле самого письма. Значение по умолчанию — **false**. |
| [get_MailSubject](./get_mailsubject/)() const | Указывает текст, который будет отображаться в строке темы электронных писем или факсов, создаваемых при слиянии почты. Значение по умолчанию — пустая строка. |
| [get_MainDocumentType](./get_maindocumenttype/)() const | Указывает тип основного документа слияния почты. Значение по умолчанию — [Default](../mailmergemaindocumenttype/). |
| [get_Odso](./get_odso/)() const | Получает объект, который указывает настройки Office Data Source Object (ODSO). |
| [get_Query](./get_query/)() const | Содержит строку Structured Query Language, которая будет выполнена против указанного внешнего источника данных для возврата набора записей, которые будут импортированы в документ при выполнении операции слияния почты. Значение по умолчанию — пустая строка. |
| [get_ViewMergedData](./get_viewmergeddata/)() const | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных там, где вставлены поля слияния (например, предварительный просмотр объединённых данных). Значение по умолчанию — **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [MailMergeSettings](./mailmergesettings/)() |  |
| [set_ActiveRecord](./set_activerecord/)(int32_t) | Указывает индекс записи из источника данных, начинающийся с 1, который будет отображаться в Microsoft Word. Значение по умолчанию — 1. |
| [set_AddressFieldName](./set_addressfieldname/)(const System::String\&) | Указывает столбец в источнике данных, содержащий адреса электронной почты. Значение по умолчанию — пустая строка. |
| [set_CheckErrors](./set_checkerrors/)(Aspose::Words::Settings::MailMergeCheckErrors) | Указывает тип отчётности об ошибках, который будет выполнять Microsoft Word при выполнении слияния почты. Значение по умолчанию — [Default](../mailmergecheckerrors/). |
| [set_ConnectString](./set_connectstring/)(const System::String\&) | Указывает строку подключения, используемую для соединения с внешним источником данных. Значение по умолчанию — пустая строка. |
| [set_DataSource](./set_datasource/)(const System::String\&) | Указывает путь к источнику данных слияния почты. Значение по умолчанию — пустая строка. |
| [set_DataType](./set_datatype/)(Aspose::Words::Settings::MailMergeDataType) | Указывает тип источника данных слияния почты и метод доступа к данным. Значение по умолчанию — [Default](../mailmergedatatype/). |
| [set_Destination](./set_destination/)(Aspose::Words::Settings::MailMergeDestination) | Указывает, как Microsoft Word будет выводить результаты слияния почты. Значение по умолчанию — [Default](../mailmergedestination/). |
| [set_DoNotSupressBlankLines](./set_donotsupressblanklines/)(bool) | Указывает, как приложение, выполняющее слияние почты, должно обрабатывать пустые строки в объединённых документах, полученных в результате слияния. Значение по умолчанию — **false**. |
| [set_HeaderSource](./set_headersource/)(const System::String\&) | Указывает путь к источнику заголовка слияния почты. Значение по умолчанию — пустая строка. |
| [set_LinkToQuery](./set_linktoquery/)(bool) | Сеттер для [Aspose::Words::Settings::MailMergeSettings::get_LinkToQuery](./get_linktoquery/). |
| [set_MailAsAttachment](./set_mailasattachment/)(bool) | Указывает, что документы, создаваемые во время операции слияния почты, должны отправляться по электронной почте в виде вложения, а не в теле самого письма. Значение по умолчанию — **false**. |
| [set_MailSubject](./set_mailsubject/)(const System::String\&) | Указывает текст, который будет отображаться в строке темы электронных писем или факсов, создаваемых при слиянии почты. Значение по умолчанию — пустая строка. |
| [set_MainDocumentType](./set_maindocumenttype/)(Aspose::Words::Settings::MailMergeMainDocumentType) | Сеттер для [Aspose::Words::Settings::MailMergeSettings::get_MainDocumentType](./get_maindocumenttype/). |
| [set_Odso](./set_odso/)(const System::SharedPtr\<Aspose::Words::Settings::Odso\>\&) | Устанавливает объект, который указывает настройки Office Data Source Object (ODSO). |
| [set_Query](./set_query/)(const System::String\&) | Содержит строку Structured Query Language, которая будет выполнена против указанного внешнего источника данных для возврата набора записей, которые будут импортированы в документ при выполнении операции слияния почты. Значение по умолчанию — пустая строка. |
| [set_ViewMergedData](./set_viewmergeddata/)(bool) | Указывает, что Microsoft Word должен отображать данные из указанного внешнего источника данных там, где вставлены поля слияния (например, предварительный просмотр объединённых данных). Значение по умолчанию — **false**. |
| static [Type](./type/)() |  |
## Примечания


Вы можете использовать этот объект, чтобы указать источник данных слияния почты для документа, и эта информация (вместе с доступными полями данных) появится в Microsoft Word, когда пользователь откроет документ. Либо вы можете использовать этот объект для запроса настроек слияния почты, которые пользователь указал в Microsoft Word для данного документа.

Обычно вам не нужно создавать объекты этого класса напрямую, потому что настройки слияния почты документа всегда доступны через свойство [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/).

Чтобы определить, является ли этот документ основным документом слияния почты, проверьте значение свойства [MainDocumentType](./get_maindocumenttype/).

Чтобы удалить настройки слияния почты и информацию о источнике данных из документа, вы можете использовать метод [Clear](./clear/). Aspose.Words не будет записывать настройки слияния почты в документ, если свойство [MainDocumentType](./get_maindocumenttype/) установлено в значение [NotAMergeDocument](../mailmergemaindocumenttype/) или свойство [DataType](./get_datatype/) установлено в значение [None](../mailmergedatatype/).

Лучший способ узнать, как использовать свойства этого объекта, — создать документ с нужным источником данных вручную в Microsoft Word, а затем открыть этот документ с помощью Aspose.Words и изучить свойства объектов [MailMergeSettings](../../aspose.words/document/get_mailmergesettings/) и [Odso](./get_odso/). Это хороший подход, если вы хотите, например, научиться программно настраивать источник данных.

Aspose.Words сохраняет информацию о слиянии почты при загрузке, сохранении и конвертации документов между разными форматами, но не использует эту информацию при выполнении собственного слияния почты с помощью объекта [MailMerge](../../aspose.words.mailmerging/mailmerge/).

## См. также

* Namespace [Aspose::Words::Settings](../)
* Library [Aspose.Words for C++](../../)
