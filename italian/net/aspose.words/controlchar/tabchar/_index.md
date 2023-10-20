---
title: ControlChar.TabChar
linktitle: TabChar
articleTitle: TabChar
second_title: Aspose.Words per .NET
description: ControlChar TabChar campo. Carattere di tabulazione char9 o t in C#.
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
