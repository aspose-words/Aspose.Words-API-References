---
title: "Aspose::Words::Fields::IFieldResultFormatter Schnittstelle"
linktitle: "IFieldResultFormatter"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldResultFormatter Schnittstelle. Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie das Feldresultat in C++ formatiert wird."
type: docs
weight: 121000
url: /de/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Implementieren Sie diese Schnittstelle, wenn Sie steuern möchten, wie das Ergebnis des Feldes formatiert wird.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Wird aufgerufen, wenn Aspose.Words einen Großschreibung-Formatwechsel anwendet, d. h. \\* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Wird aufgerufen, wenn Aspose.Words einen Zahlenformatwechsel anwendet, d. h. \\* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Wird aufgerufen, wenn Aspose.Words einen Datums-/Uhrzeitformatwechsel anwendet, d. h. \\@ \"dd.MM.yyyy\". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Wird aufgerufen, wenn Aspose.Words einen numerischen Formatwechsel anwendet, d. h. \\# \"#.##\". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
