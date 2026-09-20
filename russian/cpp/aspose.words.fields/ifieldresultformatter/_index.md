---
title: "Aspose::Words::Fields::IFieldResultFormatter интерфейс"
linktitle: "IFieldResultFormatter"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Fields::IFieldResultFormatter интерфейс. Реализуйте этот интерфейс, если хотите контролировать, как форматируется результат поля в C++."
type: docs
weight: 121000
url: /ru/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Реализуйте этот интерфейс, если хотите контролировать форматирование результата поля.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Методы

| Метод | Описание |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Вызывается, когда Aspose.Words применяет переключатель формата капитализации, т.е. \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Вызывается, когда Aspose.Words применяет переключатель числового формата, т.е. \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Вызывается, когда Aspose.Words применяет переключатель формата даты/времени, т.е. \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Вызывается, когда Aspose.Words применяет переключатель числового формата, т.е. \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## См. также

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
