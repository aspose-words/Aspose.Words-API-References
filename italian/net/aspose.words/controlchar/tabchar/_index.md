---
title: TabChar
second_title: Aspose.Words per .NET API Reference
description: Carattere di tabulazione char9 o t.
type: docs
weight: 280
url: /it/net/aspose.words/controlchar/tabchar/
---
## ControlChar.TabChar field

Carattere di tabulazione: (char)9 o "\t".

```csharp
public const char TabChar;
```

### Esempi

Mostra come impostare un intervallo personalizzato per le posizioni di tabulazione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta le tabulazioni in modo che appaiano ogni 72 punti (1 pollice).
builder.Document.DefaultTabStop = 72;

// Ciascun carattere di tabulazione fa scattare il testo dopo di esso alla posizione di arresto di tabulazione successiva più vicina.
builder.Writeln("Hello" + ControlChar.Tab + "World!");
builder.Writeln("Hello" + ControlChar.TabChar + "World!");
```

### Guarda anche

* class [ControlChar](../../controlchar)
* spazio dei nomi [Aspose.Words](../../controlchar)
* assemblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->