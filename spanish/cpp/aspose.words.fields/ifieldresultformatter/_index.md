---
title: "Aspose::Words::Fields::IFieldResultFormatter interfaz"
linktitle: "IFieldResultFormatter"
second_title: "Referencia de API de Aspose.Words para C++"
description: "Aspose::Words::Fields::IFieldResultFormatter interfaz. Implementa esta interfaz si deseas controlar cómo se formatea el resultado del campo en C++."
type: docs
weight: 121000
url: /es/cpp/aspose.words.fields/ifieldresultformatter/
---
## IFieldResultFormatter interface


Implemente esta interfaz si desea controlar cómo se formatea el resultado del campo.

```cpp
class IFieldResultFormatter : public virtual System::Object
```

## Métodos

| Método | Descripción |
| --- | --- |
| virtual [Format](./format/)(System::String, Aspose::Words::Fields::GeneralFormat) | Se llama cuando Aspose.Words aplica un interruptor de formato de capitalización, p. ej. \* Upper. |
| virtual [Format](./format/)(double, Aspose::Words::Fields::GeneralFormat) | Se llama cuando Aspose.Words aplica un interruptor de formato numérico, p. ej. \* Ordinal. |
| virtual [FormatDateTime](./formatdatetime/)(System::DateTime, System::String, Aspose::Words::CalendarType) | Se llama cuando Aspose.Words aplica un interruptor de formato de fecha/hora, p. ej. \@ "dd.MM.yyyy". |
| virtual [FormatNumeric](./formatnumeric/)(double, System::String) | Se llama cuando Aspose.Words aplica un interruptor de formato numérico, p. ej. \# "#.##". |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Ver también

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
