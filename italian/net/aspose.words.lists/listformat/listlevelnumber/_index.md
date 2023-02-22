---
title: ListFormat.ListLevelNumber
second_title: Aspose.Words per .NET API Reference
description: ListFormat proprietà. Ottiene o imposta il numero a livello di elenco da 0 a 8 per il paragrafo.
type: docs
weight: 40
url: /it/net/aspose.words.lists/listformat/listlevelnumber/
---
## ListFormat.ListLevelNumber property

Ottiene o imposta il numero a livello di elenco (da 0 a 8) per il paragrafo.

```csharp
public int ListLevelNumber { get; set; }
```

### Osservazioni

Nei documenti Word, gli elenchi possono essere costituiti da 1 o 9 livelli, numerati da 0 a 8.

Ha effetto solo quando il[`List`](../list/) la proprietà è impostata per fare riferimento a un elenco valido.

### Esempi

Mostra come lavorare con i livelli di elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare utilizzando un generatore di documenti.
// 1 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello dell'elenco
// per iniziare un sottoelenco autonomo all'elemento dell'elenco corrente.
// Il modello di elenco di Microsoft Word chiamato "NumberDefault" utilizza i numeri per creare livelli di elenco per il primo livello di elenco.
// I livelli di elenco più profondi utilizzano lettere e numeri romani minuscoli. 
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Un elenco puntato:
// Questo elenco applicherà un trattino e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "■" e "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Possiamo disabilitare la formattazione degli elenchi per non formattare i paragrafi successivi come elenchi deselezionando il flag "Elenco".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

Mostra come creare elenchi puntati e numerati.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Aspose.Words main advantages are:");

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli e rientri prefissi.
// Possiamo creare liste nidificate aumentando il livello di rientro. 
// Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti. 
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare con un generatore di documenti.
// 1 - Un elenco puntato:
// Questo elenco applicherà un trattino e un simbolo di punto elenco ("•") prima di ogni paragrafo.
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
// Gli elenchi numerati creano un ordine logico per i loro paragrafi numerando ogni elemento.
builder.ListFormat.ApplyNumberDefault();

// Questo paragrafo è il primo elemento. Il primo elemento di un elenco numerato avrà un "1". come simbolo della voce di elenco.
builder.Writeln("Opening documents from different formats:");

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Chiama il metodo "ListIndent" per aumentare il livello di elenco corrente,
// che avvierà un nuovo elenco autonomo, con un rientro più profondo, all'elemento corrente del primo livello di elenco.
builder.ListFormat.ListIndent();

Assert.AreEqual(1, builder.ListFormat.ListLevelNumber);

// Questi sono i primi tre elementi dell'elenco del secondo livello di elenco, che manterranno un conteggio
// indipendente dal conteggio del primo livello di lista. Secondo l'attuale formato dell'elenco,
// avranno i simboli di "a.", "b." e "c.".
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");

// Chiama il metodo "ListOutdent" per tornare al livello di elenco precedente.
builder.ListFormat.ListOutdent();

Assert.AreEqual(0, builder.ListFormat.ListLevelNumber);

// Questi due paragrafi continueranno il conteggio del primo livello di elenco.
// Questi elementi avranno i simboli "2." e "3".
builder.Writeln("Processing documents");
builder.Writeln("Saving documents in different formats:");

// Se aumentiamo il livello dell'elenco a un livello a cui abbiamo aggiunto elementi in precedenza,
// la lista annidata sarà separata dalla precedente e la sua numerazione partirà dall'inizio. 
// Questi elementi dell'elenco avranno i simboli di "a.", "b.", "c.", "d." ed "e".
builder.ListFormat.ListIndent();
builder.Writeln("DOC");
builder.Writeln("PDF");
builder.Writeln("HTML");
builder.Writeln("MHTML");
builder.Writeln("Plain text");

// Annulla nuovamente il livello dell'elenco.
builder.ListFormat.ListOutdent();
builder.Writeln("Doing many other things!");

// Termina l'elenco numerato.
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.ApplyDefaultBulletsAndNumbers.docx");
```

### Guarda anche

* class [ListFormat](../)
* spazio dei nomi [Aspose.Words.Lists](../../listformat/)
* assemblea [Aspose.Words](../../../)


