---
title: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond metodo"
linktitle: "Respond"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Fields::IFieldUserPromptRespondent::Respond metodo. Quando implementato, restituisce una risposta dall'utente alla richiesta. La tua implementazione dovrebbe restituire null per indicare che l'utente non ha risposto alla richiesta (cioè l'utente ha premuto il pulsante Annulla nella finestra di dialogo) in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.fields/ifielduserpromptrespondent/respond/
---
## IFieldUserPromptRespondent::Respond method


Quando implementato, restituisce una risposta dall'utente alla richiesta. La tua implementazione dovrebbe restituire **null** per indicare che l'utente non ha risposto alla richiesta (ad esempio, l'utente ha premuto il pulsante Annulla nella finestra di dialogo).

```cpp
virtual System::String Aspose::Words::Fields::IFieldUserPromptRespondent::Respond(System::String promptText, System::String defaultResponse)=0
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| promptText | System::String | Testo della richiesta (cioè titolo della finestra di dialogo). |
| defaultResponse | System::String | Risposta predefinita dell'utente (cioè valore iniziale contenuto nella finestra di dialogo). |

### ReturnValue

Risposta dell'utente (cioè valore confermato contenuto nella finestra di dialogo).

## Vedi anche

* Interface [IFieldUserPromptRespondent](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
