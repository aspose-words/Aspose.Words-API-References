---
title: "Aspose::Words::MailMerging::FieldMergingArgs class"
linktitle: "FieldMergingArgs"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::FieldMergingArgs class. Предоставляет данные для события MergeField. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 1000
url: /ru/cpp/aspose.words.mailmerging/fieldmergingargs/
---
## FieldMergingArgs class


Предоставляет данные для события **MergeField**. Чтобы узнать больше, посетите статью документации [Mail Merge and Reporting](https://docs.aspose.com/words/cpp/mail-merge-and-reporting/).

```cpp
class FieldMergingArgs : public Aspose::Words::MailMerging::FieldMergingArgsBase
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Document](../fieldmergingargsbase/get_document/)() const | Возвращает объект [Document](../fieldmergingargsbase/get_document/), для которого выполняется слияние почты. |
| [get_DocumentFieldName](../fieldmergingargsbase/get_documentfieldname/)() const | Получает имя поля слияния, как указано в документе. |
| [get_Field](../fieldmergingargsbase/get_field/)() const | Получает объект, представляющий текущее поле слияния. |
| [get_FieldName](../fieldmergingargsbase/get_fieldname/)() const | Получает имя поля слияния в источнике данных. |
| [get_FieldValue](../fieldmergingargsbase/get_fieldvalue/)() const | Получает значение поля из источника данных. |
| [get_RecordIndex](../fieldmergingargsbase/get_recordindex/)() const | Получает нулевой индекс записи, которая объединяется. |
| [get_TableName](../fieldmergingargsbase/get_tablename/)() const | Получает имя таблицы данных для текущей операции слияния или пустую строку, если имя недоступно. |
| [get_Text](./get_text/)() const | Получает или задает текст, который будет вставлен в документ для текущего поля слияния. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FieldValue](../fieldmergingargsbase/set_fieldvalue/)(const System::SharedPtr\<System::Object\>\&) | Устанавливает значение поля из источника данных. |
| [set_Text](./set_text/)(const System::String\&) | Сеттер для [Aspose::Words::MailMerging::FieldMergingArgs::get_Text](./get_text/). |
| static [Type](./type/)() |  |
## Примечания


Событие **MergeField** происходит во время слияния почты, когда в документе встречается простое поле слияния. Вы можете обработать это событие, чтобы вернуть текст, который движок слияния почты вставит в документ.

## См. также

* Class [FieldMergingArgsBase](../fieldmergingargsbase/)
* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
