---
title: Aspose::Words::Fields::IFieldResultFormatter interface
linktitle: IFieldResultFormatter
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::IFieldResultFormatter interface. Implement this interface if you want to control how the field result is formatted in C++.'
type: docs
weight: 121000
url: /cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Implement this interface if you want to control how the field result is formatted.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Called when Aspose.Words applies a capitalization format switch, i.e. \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Called when Aspose.Words applies a number format switch, i.e. \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Called when Aspose.Words applies a date/time format switch, i.e. \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Called when Aspose.Words applies a numeric format switch, i.e. \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
