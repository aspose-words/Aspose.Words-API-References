---
title: "Aspose::Words::Fields::IFieldResultFormatter 接口"
linktitle: "IFieldResultFormatter"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fields::IFieldResultFormatter 接口。如果您想在 C++ 中控制字段结果的格式化，请实现此接口。"
type: docs
weight: 121000
url: /zh/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


如果您想控制字段结果的格式化，请实现此接口。

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | 当 Aspose.Words 应用大写格式切换时调用，例如 \\* Upper。 |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | 当 Aspose.Words 应用数字格式切换时调用，例如 \\* Ordinal。 |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | 当 Aspose.Words 应用日期/时间格式切换时调用，例如 \\@ \"dd.MM.yyyy\"。 |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | 当 Aspose.Words 应用数值格式切换时调用，例如 \\# \"#.##\"。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 另见

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
