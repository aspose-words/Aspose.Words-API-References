---
title: "Aspose::Words::Fields::IFieldUpdatingProgressCallback interface"
linktitle: "IFieldUpdatingProgressCallback"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Fields::IFieldUpdatingProgressCallback interface. Implementieren Sie diese Schnittstelle, wenn Sie den Fortschritt der Feldaktualisierung in C++ verfolgen möchten."
type: docs
weight: 124000
url: /de/cpp/aspose.words.fields/ifieldupdatingprogresscallback/
---
## IFieldUpdatingProgressCallback interface


Implementieren Sie dieses Interface, wenn Sie den Fortschritt der Feldaktualisierung verfolgen möchten.

```cpp
class IFieldUpdatingProgressCallback : public virtual System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Notify](./notify/)(System::SharedPtr\<Aspose::Words::Fields::FieldUpdatingProgressArgs\>) | Eine benutzerdefinierte Methode, die aufgerufen wird, wenn sich der Aktualisierungsfortschritt ändert. |
| static [Type](./type/)() |  |
## Siehe auch

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
