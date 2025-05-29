---
title: DocumentBuilder.ListFormat
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words per .NET
description: Esplora la proprietà ListFormat di DocumentBuilder per accedere e personalizzare le impostazioni di formattazione degli elenchi correnti, per una progettazione avanzata dei documenti.
type: docs
weight: 150
url: /it/net/aspose.words/documentbuilder/listformat/
---
## DocumentBuilder.ListFormat property

Restituisce un oggetto che rappresenta le proprietà di formattazione dell'elenco corrente.

```csharp
public ListFormat ListFormat { get; }
```

## Esempi

Mostra come creare elenchi puntati e numerati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare con un generatore di documenti.
// 1 - Un elenco puntato:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
builder.ListFormat.ApplyBulletDefault();
builder.Writeln("Great performance");
builder.Writeln("High reliability");
builder.Writeln("Quality code and working");
builder.Writeln("Wide variety of features");
builder.Writeln("Easy to understand API");

// Termina l'elenco puntato.
builder.ListFormat.RemoveNumbers();

builder.InsertBreak(BreakType.ParagraphBreak);
builder.Writeln("Aspose.Words allows:");

// 2 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i paragrafi numerando ogni elemento.
builder.ListFormat.ApplyNumberDefault();

// Questo paragrafo è il primo elemento. Il primo elemento di un elenco numerato avrà un "1" come simbolo di elemento dell'elenco.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Chiama il metodo "ListIndent" per aumentare il livello dell'elenco corrente,
// che avvierà un nuovo elenco autonomo, con un rientro più profondo, all'elemento corrente del primo livello dell'elenco.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Questi sono i primi tre elementi dell'elenco del secondo livello dell'elenco, che manterranno un conteggio
// indipendente dal conteggio del primo livello dell'elenco. In base al formato dell'elenco corrente,
// avranno i simboli "a.", "b." e "c.".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Chiama il metodo "ListOutdent" per tornare al livello di elenco precedente.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Questi due paragrafi continueranno il conteggio del primo livello dell'elenco.
// Questi elementi avranno i simboli "2." e "3."
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Se aumentiamo il livello dell'elenco a un livello a cui abbiamo aggiunto elementi in precedenza,
 // l'elenco annidato sarà separato dal precedente e la sua numerazione inizierà dall'inizio.
// Questi elementi dell'elenco avranno i simboli "a.", "b.", "c.", "d." ed "e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Riduci nuovamente il rientro del livello dell'elenco.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Termina l'elenco numerato.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Guarda anche

* class [ListFormat](../../../aspose.words.lists/listformat/)
* class [DocumentBuilder](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
