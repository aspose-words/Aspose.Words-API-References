---
title: "Aspose::Words::EditorType enum"
linktitle: "EditorType"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::EditorType enum. Specifica l'insieme di possibili alias (o gruppi di modifica) che possono essere usati come alias per determinare se l'utente corrente deve essere autorizzato a modificare un singolo intervallo definito da un intervallo modificabile all'interno di un documento in C++."
type: docs
weight: 88000
url: /it/cpp/aspose.words/editortype/
---
## EditorType enum


Specifica l'insieme di possibili alias (o gruppi di modifica) che possono essere usati come alias per determinare se all'utente corrente è consentito modificare un singolo intervallo definito da un intervallo modificabile all'interno di un documento.

```cpp
enum class EditorType
```

### Valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Non specificato | 0 | Indica che il tipo di editor non è specificato. |
| Amministratori | 1 | Specifica che gli utenti associati al gruppo Amministratori saranno autorizzati a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Collaboratori | 2 | Specifica che gli utenti associati al gruppo Collaboratori saranno autorizzati a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Corrente | 3 | Specifica che gli utenti associati al gruppo Corrente saranno autorizzati a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Editor | 4 | Specifica che gli utenti associati al gruppo Editor saranno autorizzati a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Tutti | 5 | Specifica che tutti gli utenti che aprono il documento saranno autorizzati a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| None | 6 | Specifica che nessuno degli utenti che aprono il documento sarà autorizzato a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Proprietari | 7 | Specifica che gli utenti associati al gruppo Owners saranno autorizzati a modificare gli intervalli modificabili utilizzando questo tipo di modifica quando la protezione del documento è abilitata. |
| Default | n/a | Stesso di [Unspecified](./). |

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
