---
title: "Aspose::Words::Fields::IFieldResultFormatter interface"
linktitle: "IFieldResultFormatter"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IFieldResultFormatter interface. Implementera detta gränssnitt om du vill kontrollera hur fältresultatet formateras i C++."
type: docs
weight: 121000
url: /sv/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Implementera detta gränssnitt om du vill kontrollera hur fältresultatet formateras.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Kallas när Aspose.Words tillämpar en kapitaliseringsformatväxel, d.v.s. \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Kallas när Aspose.Words tillämpar en nummerformatväxel, d.v.s. \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Kallas när Aspose.Words tillämpar en datum/tid-formatväxel, d.v.s. \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Kallas när Aspose.Words tillämpar en numerisk formatväxel, d.v.s. \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
