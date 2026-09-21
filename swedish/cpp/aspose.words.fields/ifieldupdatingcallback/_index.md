---
title: "Aspose::Words::Fields::IFieldUpdatingCallback‑gränssnitt"
linktitle: "IFieldUpdatingCallback"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Fields::IFieldUpdatingCallback‑gränssnitt. Implementera detta gränssnitt om du vill ha egna anpassade metoder som anropas under en fältuppdatering i C++."
type: docs
weight: 123000
url: /sv/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implementera detta gränssnitt om du vill ha dina egna anpassade metoder som anropas under en fältuppdatering.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | En användardefinierad metod som anropas precis efter att ett fält har uppdaterats. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | En användardefinierad metod som anropas precis innan ett fält uppdateras. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Se även

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
