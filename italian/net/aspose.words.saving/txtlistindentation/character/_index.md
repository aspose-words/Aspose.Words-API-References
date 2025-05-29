---
title: TxtListIndentation.Character
linktitle: Character
articleTitle: Character
second_title: Aspose.Words per .NET
description: Scopri la proprietà TxtListIndentation per personalizzare l'indentazione degli elenchi con il tuo carattere preferito. Migliora la leggibilità e l'aspetto visivo senza sforzo!
type: docs
weight: 20
url: /it/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

Ottiene o imposta il carattere da utilizzare per l'indentazione dei livelli di elenco. Il valore predefinito è '\0', che significa che non c'è indentazione.

```csharp
public char Character { get; set; }
```

## Esempi

Mostra come configurare il rientro dell'elenco quando si salva un documento in testo normale.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Crea un elenco con tre livelli di rientro.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "Carattere" per assegnare un carattere da utilizzare
// per il padding che simula l'indentazione dell'elenco nel testo normale.
txtSaveOptions.ListIndentation.Character = ' ';

// Imposta la proprietà "Conteggio" per specificare il numero di volte
// per posizionare il carattere di riempimento per ogni livello di rientro dell'elenco.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Guarda anche

* class [TxtListIndentation](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
