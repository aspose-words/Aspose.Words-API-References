---
title: "Aspose::Words::Fields::IFieldResultFormatter interfaccia"
linktitle: "IFieldResultFormatter"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::IFieldResultFormatter interfaccia. Implementa questa interfaccia se vuoi controllare come il risultato del campo è formattato in C++."
type: docs
weight: 121000
url: /it/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Implementa questa interfaccia se desideri controllare come viene formattato il risultato del campo.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Chiamato quando Aspose.Words applica un interruttore di formato di capitalizzazione, cioè \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Chiamato quando Aspose.Words applica un interruttore di formato numerico, cioè \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Chiamato quando Aspose.Words applica un interruttore di formato data/ora, cioè \@ \"dd.MM.yyyy\". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Chiamato quando Aspose.Words applica un interruttore di formato numerico, cioè \# \"#.##\". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
