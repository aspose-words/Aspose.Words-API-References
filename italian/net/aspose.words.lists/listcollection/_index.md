---
title: ListCollection Class
linktitle: ListCollection
articleTitle: ListCollection
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Lists.ListCollection per una gestione efficiente degli elenchi puntati e numerati, migliorando la formattazione e l'organizzazione dei documenti.
type: docs
weight: 3920
url: /it/net/aspose.words.lists/listcollection/
---
## ListCollection class

Memorizza e gestisce la formattazione degli elenchi puntati e numerati utilizzati in un documento.

Per saperne di più, visita il[Lavorare con gli elenchi](https://docs.aspose.com/words/net/working-with-lists/) articolo di documentazione.

```csharp
public class ListCollection : IEnumerable<List>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words.lists/listcollection/count/) { get; } | Ottiene il conteggio degli elenchi numerati e puntati nel documento. |
| [Document](../../aspose.words.lists/listcollection/document/) { get; } | Ottiene il documento del proprietario. |
| [Item](../../aspose.words.lists/listcollection/item/) { get; } | Ottiene un elenco per indice. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Add](../../aspose.words.lists/listcollection/add/#add)(*[ListTemplate](../listtemplate/)*) | Crea un nuovo elenco basato su un modello predefinito e lo aggiunge alla raccolta di elenchi nel documento. |
| [Add](../../aspose.words.lists/listcollection/add/#add_1)(*[Style](../../aspose.words/style/)*) | Crea un nuovo elenco che fa riferimento a uno stile di elenco e lo aggiunge alla raccolta di elenchi nel documento. |
| [AddCopy](../../aspose.words.lists/listcollection/addcopy/)(*[List](../list/)*) | Crea un nuovo elenco copiando l'elenco specificato e aggiungendolo alla raccolta di elenchi nel documento. |
| [AddSingleLevelList](../../aspose.words.lists/listcollection/addsinglelevellist/)(*[ListTemplate](../listtemplate/)*) | Crea un nuovo elenco a livello singolo basato sul modello predefinito e lo aggiunge alla raccolta di elenchi nel documento. |
| [GetEnumerator](../../aspose.words.lists/listcollection/getenumerator/)() | Ottiene l'oggetto enumeratore che enumererà gli elenchi nel documento. |
| [GetListByListId](../../aspose.words.lists/listcollection/getlistbylistid/)(*int*) | Ottiene un elenco tramite un identificatore di elenco. |

## Osservazioni

Un elenco in un documento di Microsoft Word è un insieme di proprietà di formattazione degli elenchi. La formattazione degli elenchi è memorizzata nel`ListCollection` raccolta separatamente dai paragrafi di testo.

Non si creano oggetti di questa classe. Ce n'è sempre solo uno.`ListCollection` oggetto per documento ed è accessibile tramite[`Lists`](../../aspose.words/documentbase/lists/) proprietà.

Per creare un nuovo elenco basato su un modello di elenco predefinito o su uno stile di elenco, utilizzare [`Add`](./add/) metodo.

Per creare un nuovo elenco con formattazione identica a un elenco esistente, utilizzare[`AddCopy`](./addcopy/) metodo.

Per rendere un paragrafo puntato o numerato, è necessario applicare la formattazione di elenco a un paragrafo assegnando un[`List`](../list/)oggetto a the [`List`](../listformat/list/) proprietà di[`ListFormat`](../listformat/).

Per rimuovere la formattazione dell'elenco da un paragrafo, utilizzare[`RemoveNumbers`](../listformat/removenumbers/) Metodo .

Se conoscete un po' di WordprocessingML, saprete che definisce concetti separati per "elenco" e "definizione di elenco". Questo corrisponde esattamente a come la formattazione di un elenco viene memorizzata a basso livello in un documento Microsoft Word. La definizione di un elenco è come uno "schema" e l'elenco è come un'istanza di una definizione di elenco.

Per semplificare il modello di programmazione, Aspose.Words nasconde la distinzione tra la definizione list e list nello stesso modo in cui Microsoft Word la nasconde nella sua interfaccia utente. Ciò consente di concentrarsi maggiormente su come si desidera che appaia il documento, anziché creare oggetti di basso livello per soddisfare i requisiti del formato file Microsoft Word.

Nella versione corrente di Aspose.Words. non è possibile eliminare gli elenchi una volta creati. Ciò è simile a Microsoft Word, in cui l'utente non ha un controllo esplicito sulle definizioni degli elenchi.

## Esempi

Mostra come creare un documento con un campione di tutti gli elenchi di un altro documento.

```csharp
public void PrintOutAllLists()
{
    Document srcDoc = new Document(MyDir + "Rendering.docx");

    Document dstDoc = new Document();
    DocumentBuilder builder = new DocumentBuilder(dstDoc);

    foreach (List srcList in srcDoc.Lists)
    {
        List dstList = dstDoc.Lists.AddCopy(srcList);
        AddListSample(builder, dstList);
    }

    dstDoc.Save(ArtifactsDir + "Lists.PrintOutAllLists.docx");
}

private static void AddListSample(DocumentBuilder builder, List list)
{
    builder.Writeln("Sample formatting of list with ListId:" + list.ListId);
    builder.ListFormat.List = list;
    for (int i = 0; i < list.ListLevels.Count; i++)
    {
        builder.ListFormat.ListLevelNumber = i;
        builder.Writeln("Level " + i);
    }

    builder.ListFormat.RemoveNumbers();
    builder.Writeln();
}
```

Mostra come riavviare la numerazione in un elenco copiando l'elenco stesso.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizzane il primo livello.
List list1 = doc.Lists.Add(ListTemplate.NumberArabicParenthesis);
list1.ListLevels[0].Font.Color = Color.Red;
list1.ListLevels[0].Alignment = ListLevelAlignment.Right;

// Applichiamo il nostro elenco ad alcuni paragrafi.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("List 1 starts below:");
builder.ListFormat.List = list1;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

// Possiamo aggiungere una copia di un elenco esistente alla raccolta di elenchi del documento
// per creare un elenco simile senza apportare modifiche all'originale.
List list2 = doc.Lists.AddCopy(list1);
list2.ListLevels[0].Font.Color = Color.Blue;
list2.ListLevels[0].StartAt = 10;

// Applica il secondo elenco ai nuovi paragrafi.
builder.Writeln("List 2 starts below:");
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

doc.Save(ArtifactsDir + "Lists.RestartNumberingUsingListCopy.docx");
```

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

* class [List](../list/)
* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)
