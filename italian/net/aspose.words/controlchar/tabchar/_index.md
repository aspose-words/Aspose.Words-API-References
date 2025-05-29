---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words per .NET
description: Padroneggia i campi TabChar con ControlChar per una gestione dati fluida. Sblocca l'efficienza con il versatile carattere di tabulazione (char9 o t) oggi stesso!
type: docs
weight: 280
url: /it/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Carattere di tabulazione: (char)9 o "\t".

```csharp
public const char TabChar;
```

## Esempi

Mostra come impostare un intervallo personalizzato per le posizioni di tabulazione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta le tabulazioni in modo che appaiano ogni 72 punti (1 pollice).
builder.Document.DefaultTabStop = 72;

// Ogni carattere di tabulazione sposta il testo successivo nella posizione di tabulazione più vicina.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Guarda anche

* class [ControlChar](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
