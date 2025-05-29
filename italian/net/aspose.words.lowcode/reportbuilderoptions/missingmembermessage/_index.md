---
title: ReportBuilderOptions.MissingMemberMessage
linktitle: MissingMemberMessage
articleTitle: MissingMemberMessage
second_title: Aspose.Words per .NET
description: Scopri la proprietà MissingMemberMessage di ReportBuilderOptions. Personalizza facilmente i messaggi per i riferimenti a oggetti mancanti, migliorando l'esperienza utente senza sforzo.
type: docs
weight: 30
url: /it/net/aspose.words.lowcode/reportbuilderoptions/missingmembermessage/
---
## ReportBuilderOptions.MissingMemberMessage property

Ottiene o imposta un valore stringa stampato al posto di un'espressione modello che rappresenta un semplice riferimento a , un membro mancante di un oggetto. Il valore predefinito è una stringa vuota.

```csharp
public string MissingMemberMessage { get; set; }
```

## Osservazioni

La proprietà dovrebbe essere utilizzata insieme aAllowMissingMembers Opzione . In caso contrario, viene generata un'eccezione quando viene rilevato un elemento mancante di un oggetto.

La proprietà influisce solo sulla stampa di un'espressione modello che rappresenta un semplice riferimento a un membro dell'oggetto missing . Ad esempio, la stampa di un operatore binario, uno dei cui operandi fa riferimento a un membro dell'oggetto missing , non è interessata.

Il valore di questa proprietà non può essere impostato su null.

### Guarda anche

* class [ReportBuilderOptions](../)
* spazio dei nomi [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* assemblea [Aspose.Words](../../../)
