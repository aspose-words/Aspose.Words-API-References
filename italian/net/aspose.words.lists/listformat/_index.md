---
title: Class ListFormat
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Lists.ListFormat classe. Permette di controllare quale formattazione dellelenco viene applicata a un paragrafo.
type: docs
weight: 3480
url: /it/net/aspose.words.lists/listformat/
---
## ListFormat class

Permette di controllare quale formattazione dell'elenco viene applicata a un paragrafo.

Per saperne di più, visita il[Lavorare con gli elenchi](https://docs.aspose.com/words/net/working-with-lists/) articolo di documentazione.

```csharp
public class ListFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Vero quando al paragrafo è applicata la formattazione puntata o numerata. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Ottiene o imposta l'elenco di cui questo paragrafo è membro. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Restituisce la formattazione a livello di elenco più eventuali sostituzioni di formattazione applicate al paragrafo corrente. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Ottiene o imposta il numero del livello di elenco (da 0 a 8) per il paragrafo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Avvia un nuovo elenco puntato predefinito e lo applica al paragrafo. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Avvia un nuovo elenco numerato predefinito e lo applica al paragrafo. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Aumenta di un livello il livello dell'elenco del paragrafo corrente. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Diminuisce di un livello il livello dell'elenco del paragrafo corrente. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Rimuove numeri o punti elenco dal paragrafo corrente e imposta il livello dell'elenco su zero. |

### Osservazioni

Un paragrafo in un documento di Microsoft Word può essere puntato o numerato. Quando un paragrafo è puntato o numerato, si dice che al paragrafo viene applicata la formattazione elenco .

Non crei oggetti del`ListFormat` classe direttamente. Accedi`ListFormat` come proprietà di un altro oggetto a cui può essere associata la formattazione dell'elenco. Al momento gli oggetti che possono avere la formattazione lista sono:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) E[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` di un[`Paragraph`](../../aspose.words/paragraph/) specifica quale formattazione dell'elenco e livello dell'elenco vengono applicati a quel particolare paragrafo.

`ListFormat` di un[`Style`](../../aspose.words/style/) (applicable solo agli stili di paragrafo) consente di specificare quale formattazione dell'elenco e livello elenco viene applicato a tutti i paragrafi di quel particolare stile.

`ListFormat` di un[`DocumentBuilder`](../../aspose.words/documentbuilder/) fornisce l'accesso alla formattazione dell'elenco nella posizione corrente del cursore all'interno del[`DocumentBuilder`](../../aspose.words/documentbuilder/).

La formattazione stessa dell'elenco è memorizzata all'interno di un file[`List`](../list/) Oggetto archiviato separatamente dai paragrafi. L'elenco degli oggetti è archiviato all'interno di un file[`ListCollection`](../listcollection/) collezione. C'è un singolo [`ListCollection`](../listcollection/) raccolta per[`Document`](../../aspose.words/document/).

I paragrafi non appartengono fisicamente a un elenco. I paragrafi just fanno riferimento a un particolare oggetto elenco tramite il file[`List`](./list/) property e un particolare livello nell'elenco tramite il file[`ListLevelNumber`](./listlevelnumber/) property. Impostando queste due proprietà puoi controllare quali punti elenco e numerazioni vengono applicati a un paragrafo.

### Esempi

Mostra come lavorare con i livelli di elenco.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Un elenco ci consente di organizzare e decorare insiemi di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi nidificati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" del generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento nell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare utilizzando un generatore di documenti.
// 1 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i paragrafi numerando ciascun elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello della lista
// per iniziare un sottoelenco autonomo dall'elemento dell'elenco corrente.
// Il modello di elenco di Microsoft Word denominato "NumberDefault" utilizza i numeri per creare livelli di elenco per il primo livello di elenco.
 // I livelli di elenco più profondi utilizzano lettere e numeri romani minuscoli.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Un elenco puntato:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "***" e "○".
builder.ListFormat.List = doc.Lists.Add(ListTemplate.BulletDefault);

for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// Possiamo disabilitare la formattazione dell'elenco per non formattare i paragrafi successivi come elenchi deselezionando il flag "Elenco".
builder.ListFormat.List = null;

Assert.False(builder.ListFormat.IsListItem);

doc.Save(ArtifactsDir + "Lists.SpecifyListLevel.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)


