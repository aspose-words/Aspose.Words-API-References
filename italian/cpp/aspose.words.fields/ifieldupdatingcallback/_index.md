---
title: "Interfaccia Aspose::Words::Fields::IFieldUpdatingCallback"
linktitle: "IFieldUpdatingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Interfaccia Aspose::Words::Fields::IFieldUpdatingCallback. Implementa questa interfaccia se desideri avere i tuoi metodi personalizzati chiamati durante l'aggiornamento di un campo in C++."
type: docs
weight: 123000
url: /it/cpp/aspose.words.fields/ifieldupdatingcallback/
---
## IFieldUpdatingCallback interface


Implementa questa interfaccia se desideri avere i tuoi metodi personalizzati chiamati durante l'aggiornamento di un campo.

```cpp
class IFieldUpdatingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| virtual [FieldUpdated](./fieldupdated/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Un metodo definito dall'utente che viene chiamato subito dopo che un campo è stato aggiornato. |
| virtual [FieldUpdating](./fieldupdating/)(System::SharedPtr\<Aspose::Words::Fields::Field\>) | Un metodo definito dall'utente che viene chiamato subito prima che un campo sia aggiornato. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
