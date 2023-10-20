---
title: ControlChar.Tab
linktitle: Tab
articleTitle: Tab
second_title: Aspose.Words per .NET
description: ControlChar Tab campo. Carattere di tabulazione x0009 o t in C#.
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

Mostra come impostare un intervallo personalizzato per le posizioni dei punti di tabulazione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta le tabulazioni in modo che vengano visualizzate ogni 72 punti (1 pollice).
builder.Document.DefaultTabStop = 72;

// Ogni carattere di tabulazione fa scattare il testo successivo alla posizione di tabulazione successiva più vicina.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Guarda anche

* class [ControlChar](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
