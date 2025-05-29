---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words per .NET
description: Scopri il campo Tab ControlChar e scopri il carattere Tab x0009 per una formattazione efficiente del testo e una gestione avanzata dei dati.
type: docs
weight: 270
url: /it/net/aspose.words/controlchar/tab/
---
## ControlChar.Tab field

Carattere di tabulazione: "\x0009" o "\t".

```csharp
public static readonly string Tab;
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
