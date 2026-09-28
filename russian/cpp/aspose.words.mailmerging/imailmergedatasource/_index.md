---
title: "Aspose::Words::MailMerging::IMailMergeDataSource интерфейс"
linktitle: "IMailMergeDataSource"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::MailMerging::IMailMergeDataSource интерфейс. Реализуйте этот интерфейс, чтобы позволить слияние писем из пользовательского источника данных, например списка объектов. Данные мастер‑деталь также поддерживаются в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.mailmerging/imailmergedatasource/
---
## IMailMergeDataSource interface


Реализуйте этот интерфейс, чтобы разрешить слияние почты из пользовательского источника данных, например списка объектов. Данные мастер‑деталь также поддерживаются.

```cpp
class IMailMergeDataSource : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [get_TableName](./get_tablename/)() | Возвращает имя источника данных. |
| virtual [GetChildDataSource](./getchilddatasource/)(System::String) | Движок слияния писем Aspose.Words вызывает этот метод, когда встречает начало вложенного региона слияния писем. |
| [GetType](./gettype/)() const override |  |
| virtual [GetValue](./getvalue/)(System::String, System::SharedPtr\<System::Object\>\&) |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [MoveNext](./movenext/)() | Переходит к следующей записи в источнике данных. |
| static [Type](./type/)() |  |
## Примечания


Когда создаётся источник данных, его следует инициализировать, указывая на BOF (до первой записи). Движок слияния писем Aspose.Words вызовет [MoveNext](./movenext/), чтобы перейти к следующей записи, а затем вызовет [GetValue()](./getvalue/) для каждого поля слияния, которое он встретит в документе или текущем регионе слияния писем.

## См. также

* Namespace [Aspose::Words::MailMerging](../)
* Library [Aspose.Words for C++](../../)
