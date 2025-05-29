---
title: ListFormat Class
linktitle: ListFormat
articleTitle: ListFormat
second_title: Aspose.Words per .NET
description: Formattazione degli elenchi master nei tuoi documenti con la classe Aspose.Words.Lists.ListFormat. Migliora facilmente lo stile dei paragrafi per una migliore leggibilità.
type: docs
weight: 3930
url: /it/net/aspose.words.lists/listformat/
---
## ListFormat class

Consente di controllare quale formattazione di elenco viene applicata a un paragrafo.

Per saperne di più, visita il[Lavorare con gli elenchi](https://docs.aspose.com/words/net/working-with-lists/) articolo di documentazione.

```csharp
public class ListFormat
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [IsListItem](../../aspose.words.lists/listformat/islistitem/) { get; } | Vero quando al paragrafo è stata applicata la formattazione puntata o numerata. |
| [List](../../aspose.words.lists/listformat/list/) { get; set; } | Ottiene o imposta l'elenco di cui questo paragrafo è membro. |
| [ListLevel](../../aspose.words.lists/listformat/listlevel/) { get; } | Restituisce la formattazione a livello di elenco più eventuali sovrascritture di formattazione applicate al paragrafo corrente. |
| [ListLevelNumber](../../aspose.words.lists/listformat/listlevelnumber/) { get; set; } | Ottiene o imposta il numero del livello di elenco (da 0 a 8) per il paragrafo. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [ApplyBulletDefault](../../aspose.words.lists/listformat/applybulletdefault/)() | Avvia un nuovo elenco puntato predefinito e lo applica al paragrafo. |
| [ApplyNumberDefault](../../aspose.words.lists/listformat/applynumberdefault/)() | Avvia un nuovo elenco numerato predefinito e lo applica al paragrafo. |
| [ListIndent](../../aspose.words.lists/listformat/listindent/)() | Aumenta di un livello il livello dell'elenco del paragrafo corrente. |
| [ListOutdent](../../aspose.words.lists/listformat/listoutdent/)() | Diminuisce di un livello il livello dell'elenco del paragrafo corrente. |
| [RemoveNumbers](../../aspose.words.lists/listformat/removenumbers/)() | Rimuove numeri o elenchi puntati dal paragrafo corrente e imposta il livello dell'elenco su zero. |

## Osservazioni

Un paragrafo in un documento Microsoft Word può essere puntato o numerato. Quando un paragrafo è puntato o numerato, si dice che al paragrafo viene applicata la formattazione di elenco.

Non si creano oggetti del`ListFormat` classe direttamente. Accedi`ListFormat`Come proprietà di un altro oggetto a cui è associata la formattazione di elenco. Al momento, gli oggetti a cui è associata la formattazione di elenco sono:[`Paragraph`](../../aspose.words/paragraph/) , [`Style`](../../aspose.words/style/) E[`DocumentBuilder`](../../aspose.words/documentbuilder/).

`ListFormat` di un[`Paragraph`](../../aspose.words/paragraph/) specifica quale formattazione e livello di elenco vengono applicati a quel particolare paragrafo.

`ListFormat` di un[`Style`](../../aspose.words/style/) (applicable solo agli stili di paragrafo) consente di specificare quale formattazione di elenco e livello di elenco vengono applicati a tutti i paragrafi di quello stile particolare.

`ListFormat` di un[`DocumentBuilder`](../../aspose.words/documentbuilder/) fornisce l'accesso alla formattazione dell'elenco nella posizione corrente del cursore all'interno dell'[`DocumentBuilder`](../../aspose.words/documentbuilder/).

La formattazione dell'elenco stesso è memorizzata all'interno di un[`List`](../list/) Oggetto memorizzato separatamente dai paragrafi. Gli oggetti elenco sono memorizzati all'interno di un[`ListCollection`](../listcollection/) collezione. C'è un singolo [`ListCollection`](../listcollection/) raccolta per[`Document`](../../aspose.words/document/).

paragrafi non appartengono fisicamente a un elenco. I paragrafi fanno semplicemente riferimento a un particolare oggetto elenco tramite[`List`](./list/) property e un livello particolare nell'elenco tramite il[`ListLevelNumber`](./listlevelnumber/) property. Impostando queste due proprietà puoi controllare quali elenchi puntati e numerati vengono applicati a un paragrafo.

## Esempi

Mostra come lavorare con i livelli degli elenchi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.False(builder.ListFormat.IsListItem);

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Di seguito sono riportati due tipi di elenchi che possiamo creare utilizzando un generatore di documenti.
// 1 - Un elenco numerato:
// Gli elenchi numerati creano un ordine logico per i paragrafi numerando ogni elemento.
builder.ListFormat.List = doc.Lists.Add(ListTemplate.NumberDefault);

Assert.True(builder.ListFormat.IsListItem);

// Impostando la proprietà "ListLevelNumber", possiamo aumentare il livello dell'elenco
// per iniziare un sottoelenco autonomo a partire dall'elemento corrente dell'elenco.
// Il modello di elenco di Microsoft Word denominato "NumberDefault" utilizza i numeri per creare livelli di elenco per il primo livello di elenco.
 // I livelli più profondi dell'elenco utilizzano lettere e numeri romani minuscoli.
for (int i = 0; i < 9; i++)
{
    builder.ListFormat.ListLevelNumber = i;
    builder.Writeln("Level " + i);
}

// 2 - Un elenco puntato:
// Questo elenco applicherà un rientro e un simbolo di punto elenco ("•") prima di ogni paragrafo.
// I livelli più profondi di questo elenco utilizzeranno simboli diversi, come "■" e "○".
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
