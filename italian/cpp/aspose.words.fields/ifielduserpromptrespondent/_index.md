---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent interfaccia"
linktitle: "IFieldUserPromptRespondent"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent interfaccia. Rappresenta il rispondente alle richieste dell'utente durante l'aggiornamento del campo in C++."
type: docs
weight: 125000
url: /it/cpp/aspose.words.fields/ifielduserpromptrespondent/
---
## IFieldUserPromptRespondent interface


Rappresenta il rispondente alle richieste dell'utente durante l'aggiornamento del campo.

```cpp
class IFieldUserPromptRespondent : public virtual System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [Respond](./respond/)(System::String, System::String) | Quando implementato, restituisce una risposta dall'utente alla richiesta. La tua implementazione dovrebbe restituire **null** per indicare che l'utente non ha risposto alla richiesta (ad esempio, l'utente ha premuto il pulsante Annulla nella finestra di dialogo). |
| static [Type](./type/)() |  |
## Vedi anche

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words for C++](../../)
