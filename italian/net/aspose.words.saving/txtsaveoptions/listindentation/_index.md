---
title: TxtSaveOptions.ListIndentation
second_title: Aspose.Words per .NET API Reference
description: TxtSaveOptions proprietà. Ottiene un oggetto ListIndentation che specifica quanti e quali caratteri utilizzare per il rientro dei livelli di elenco. Per impostazione predefinita il conteggio dei caratteri 0 è zero ciò significa nessun rientro.
type: docs
weight: 30
url: /it/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Ottiene un oggetto ListIndentation che specifica quanti e quali caratteri utilizzare per il rientro dei livelli di elenco. Per impostazione predefinita, il conteggio dei caratteri '\0' è zero, ciò significa nessun rientro.

```csharp
public TxtListIndentation ListIndentation { get; }
```

### Esempi

Mostra come configurare il rientro dell'elenco quando si salva un documento come testo normale.

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

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento come testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "Carattere" per assegnare un carattere da usare
// per il riempimento che simula il rientro dell'elenco in testo normale.
txtSaveOptions.ListIndentation.Character = ' ';

// Imposta la proprietà "Count" per specificare il numero di volte
// per posizionare il carattere di riempimento per ogni livello di rientro dell'elenco.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Guarda anche

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../txtsaveoptions/)
* assemblea [Aspose.Words](../../../)


