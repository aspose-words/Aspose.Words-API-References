---
title: "واجهة Aspose::Words::Fields::IFieldResultFormatter"
linktitle: "IFieldResultFormatter"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "واجهة Aspose::Words::Fields::IFieldResultFormatter. نفّذ هذه الواجهة إذا أردت التحكم في كيفية تنسيق نتيجة الحقل في C++."
type: docs
weight: 121000
url: /ar/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


نفّذ هذه الواجهة إذا أردت التحكم في كيفية تنسيق نتيجة الحقل.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | يتم استدعاؤه عندما تقوم Aspose.Words بتطبيق مفتاح تنسيق الحروف الكبيرة، أي \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | يتم استدعاؤه عندما تقوم Aspose.Words بتطبيق مفتاح تنسيق الأرقام، أي \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | يتم استدعاؤه عندما تقوم Aspose.Words بتطبيق مفتاح تنسيق التاريخ/الوقت، أي \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | يتم استدعاؤه عندما تقوم Aspose.Words بتطبيق مفتاح تنسيق رقمي، أي \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## انظر أيضًا

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
