---
title: ListFormat.RemoveNumbers
linktitle: RemoveNumbers
articleTitle: RemoveNumbers
second_title: Aspose.Words per .NET
description: ListFormat RemoveNumbers metodo. Rimuove numeri o punti elenco dal paragrafo corrente e imposta il livello dellelenco su zero in C#.
type: docs
weight: 90
url: /it/net/aspose.words.lists/listformat/removenumbers/
---
## ListFormat.RemoveNumbers method

Rimuove numeri o punti elenco dal paragrafo corrente e imposta il livello dell'elenco su zero.

```csharp
public void RemoveNumbers()
```

## Osservazioni

Chiamare questo metodo equivale a impostare il file[`List`](../list/) proprietà a`nullo`.

## Esempi

Mostra come rimuovere la formattazione dell'elenco da tutti i paragrafi nel testo principale di una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Numbered list item 1");
builder.Writeln("Numbered list item 2");
builder.Writeln("Numbered list item 3");
builder.ListFormat.RemoveNumbers();

NodeCollection paras = doc.GetChildNodes(NodeType.Paragraph, true);
Assert.AreEqual(3, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));

foreach (Paragraph paragraph in paras)
    paragraph.ListFormat.RemoveNumbers();

Assert.AreEqual(0, paras.Count(n => (n as Paragraph).ListFormat.IsListItem));
```

Mostra come creare elenchi puntati e numerati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
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
// Gli elenchi numerati creano un ordine logico per i paragrafi numerando ciascun elemento.
builder.ListFormat.ApplyNumberDefault();

// Questo paragrafo è il primo elemento. Il primo elemento di un elenco numerato avrà un "1". come simbolo della voce di elenco.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Chiama il metodo "ListIndent" per aumentare il livello dell'elenco corrente,
// che inizierà un nuovo elenco autonomo, con un rientro più profondo, in corrispondenza dell'elemento corrente del primo livello dell'elenco.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Questi sono i primi tre elementi dell'elenco del secondo livello dell'elenco, che manterranno un conteggio
// indipendente dal conteggio del primo livello dell'elenco. Secondo l'attuale formato dell'elenco,
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

// Riduci nuovamente il livello dell'elenco.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Termina l'elenco numerato.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Guarda anche

* class [ListFormat](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
