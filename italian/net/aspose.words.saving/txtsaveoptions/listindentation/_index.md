---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: Aspose.Words per .NET
description: Scopri la proprietà ListIndentation di TxtSaveOptions, che personalizza l'indentazione degli elenchi per una migliore leggibilità. Controlla caratteri e livelli senza sforzo!
type: docs
weight: 30
url: /it/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Ottiene un[`TxtListIndentation`](../../txtlistindentation/)oggetto che specifica quanti e quali caratteri utilizzare per l'indentazione dei livelli di elenco. Per impostazione predefinita, il conteggio del carattere '\0' è zero, il che significa nessuna indentazione.

```csharp
public TxtListIndentation ListIndentation { get; }
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

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
