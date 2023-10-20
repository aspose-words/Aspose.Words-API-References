---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words per .NET
description: Aspose.Words.Saving.TxtListIndentation classe. Specifica il rientro dei livelli dellelenco durante lesportazione del documentoText formato in C#.
type: docs
weight: 5650
url: /it/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Specifica il rientro dei livelli dell'elenco durante l'esportazione del documentoText formato.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class TxtListIndentation
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Ottiene o imposta il carattere da utilizzare per il rientro dei livelli dell'elenco. Il valore predefinito è '\0', ciò significa che non c'è rientro. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Ottiene o imposta il numero[`Character`](./character/) da utilizzare come rientro per un livello di elenco. Il valore predefinito è 0, ciò significa nessun rientro. |

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

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Imposta la proprietà "Carattere" per assegnare un carattere da utilizzare
// per il riempimento che simula il rientro dell'elenco nel testo normale.
txtSaveOptions.ListIndentation.Character = ' ';

// Imposta la proprietà "Count" per specificare il numero di volte
// per posizionare il carattere di riempimento per ciascun livello di rientro dell'elenco.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
