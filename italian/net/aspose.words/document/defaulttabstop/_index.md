---
title: Document.DefaultTabStop
linktitle: DefaultTabStop
articleTitle: DefaultTabStop
second_title: Aspose.Words per .NET
description: Document DefaultTabStop proprietà. Ottiene o imposta lintervallo in punti tra le tabulazioni predefinite in C#.
type: docs
weight: 90
url: /it/net/aspose.words/document/defaulttabstop/
---
## Document.DefaultTabStop property

Ottiene o imposta l'intervallo (in punti) tra le tabulazioni predefinite.

```csharp
public double DefaultTabStop { get; set; }
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

* class [TabStopCollection](../../tabstopcollection/)
* class [TabStop](../../tabstop/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
