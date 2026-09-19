---
title: "Interfaccia Aspose::Words::Replacing::IReplacingCallback"
linktitle: "IReplacingCallback"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::IReplacingCallback interfaccia. Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante un'operazione di ricerca e sostituzione in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words.replacing/ireplacingcallback/
---
## IReplacingCallback interface


Implementa questa interfaccia se desideri avere il tuo metodo personalizzato chiamato durante un'operazione di ricerca e sostituzione.

```cpp
class IReplacingCallback : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Replacing](./replacing/)(System::SharedPtr\<Aspose::Words::Replacing::ReplacingArgs\>) | Un metodo definito dall'utente che viene chiamato durante un'operazione di sostituzione per ogni corrispondenza trovata appena prima che avvenga la sostituzione. |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Replacing](../)
* Library [Aspose.Words for C++](../../)
