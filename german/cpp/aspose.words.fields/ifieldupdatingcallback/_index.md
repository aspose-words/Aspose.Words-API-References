---
title: "Aspose::Words::Fields::IFieldUpdatingCallback interface"
linktitle: "IFieldUpdatingCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldUpdatingCallback interface. Implementieren Sie dieses Interface, wenn Sie eigene benutzerdefinierte Methoden während einer Feldaktualisierung in C++ aufrufen möchten."
type: docs
weight: 123000
url: /de/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implementieren Sie diese Schnittstelle, wenn Sie eigene benutzerdefinierte Methoden während einer Feldaktualisierung aufrufen lassen möchten.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Eine benutzerdefinierte Methode, die unmittelbar nach der Aktualisierung eines Feldes aufgerufen wird. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Eine benutzerdefinierte Methode, die unmittelbar vor der Aktualisierung eines Feldes aufgerufen wird. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
