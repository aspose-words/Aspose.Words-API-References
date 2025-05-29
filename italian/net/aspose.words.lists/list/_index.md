---
title: List Class
linktitle: List
articleTitle: List
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Lists.List per una formattazione potente degli elenchi. Migliora i tuoi documenti con un'organizzazione impeccabile e una presentazione professionale.
type: docs
weight: 3910
url: /it/net/aspose.words.lists/list/
---
## List class

Rappresenta la formattazione di un elenco.

Per saperne di più, visita il[Lavorare con gli elenchi](https://docs.aspose.com/words/net/working-with-lists/) articolo di documentazione.

```csharp
public class List : IComparable<List>
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Document](../../aspose.words.lists/list/document/) { get; } | Ottiene il documento del proprietario. |
| [IsListStyleDefinition](../../aspose.words.lists/list/isliststyledefinition/) { get; } | Restituisce`VERO` se questo elenco è una definizione di uno stile di elenco. |
| [IsListStyleReference](../../aspose.words.lists/list/isliststylereference/) { get; } | Restituisce`VERO` se questo elenco è un riferimento a uno stile di elenco. |
| [IsMultiLevel](../../aspose.words.lists/list/ismultilevel/) { get; } | Restituisce`VERO` quando l'elenco contiene 9 livelli;`falso` quando 1 livello. |
| [IsRestartAtEachSection](../../aspose.words.lists/list/isrestartateachsection/) { get; set; } | Specifica se l'elenco deve essere riavviato a ogni sezione. Il valore predefinito è`falso` . |
| [ListId](../../aspose.words.lists/list/listid/) { get; } | Ottiene l'identificatore univoco dell'elenco. |
| [ListLevels](../../aspose.words.lists/list/listlevels/) { get; } | Ottiene la raccolta dei livelli di elenco per questo elenco. |
| [Style](../../aspose.words.lists/list/style/) { get; } | Ottiene lo stile di elenco a cui questo elenco fa riferimento o che definisce. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto)(*List*) | Confronta l'elenco specificato con l'elenco corrente. |
| [CompareTo](../../aspose.words.lists/list/compareto/#compareto_1)(*object*) | Confronta l'oggetto specificato con l'oggetto corrente. |
| [Equals](../../aspose.words.lists/list/equals/#equals)(*List*) | Confronta con l'elenco specificato. |
| override [Equals](../../aspose.words.lists/list/equals/#equals_1)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |
| override [GetHashCode](../../aspose.words.lists/list/gethashcode/)() | Calcola il codice hash per questo oggetto elenco. |
| [HasSameTemplate](../../aspose.words.lists/list/hassametemplate/)(*List*) | Restituisce true se l'elenco corrente e l'elenco specificato vengono creati dallo stesso modello. |

## Osservazioni

Un elenco in un documento Microsoft Word è un insieme di proprietà di formattazione dell'elenco. Ogni elenco può avere fino a 9 livelli e le proprietà di formattazione, come lo stile del numero, il valore iniziale, il rientro, la posizione della tabulazione ecc., sono definite separatamente per ogni livello.

UN`List` l'oggetto appartiene sempre a[`ListCollection`](../listcollection/) collezione.

Per creare un nuovo elenco, utilizzare i metodi Add di[`ListCollection`](../listcollection/) collezione.

Per modificare la formattazione di un elenco, utilizzare[`ListLevel`](../listlevel/) oggetti trovati in il[`ListLevels`](./listlevels/) collezione.

Per applicare o rimuovere la formattazione dell'elenco da un paragrafo, utilizzare[`ListFormat`](../listformat/).

## Esempi

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

Mostra come applicare la formattazione personalizzata degli elenchi ai paragrafi quando si utilizza DocumentBuilder.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Crea un elenco da un modello di Microsoft Word e personalizza i primi due livelli dell'elenco.
List list = doc.Lists.Add(ListTemplate.NumberDefault);

ListLevel listLevel = list.ListLevels[0];
listLevel.Font.Color = Color.Red;
listLevel.Font.Size = 24;
listLevel.NumberStyle = NumberStyle.OrdinalText;
listLevel.StartAt = 21;
listLevel.NumberFormat = "\x0000";

listLevel.NumberPosition = -36;
listLevel.TextPosition = 144;
listLevel.TabPosition = 144;

listLevel = list.ListLevels[1];
listLevel.Alignment = ListLevelAlignment.Right;
listLevel.NumberStyle = NumberStyle.Bullet;
listLevel.Font.Name = "Wingdings";
listLevel.Font.Color = Color.Blue;
listLevel.Font.Size = 24;

// Questo valore NumberFormat creerà simboli di elenchi puntati a forma di stella.
listLevel.NumberFormat = "\xf0af";
listLevel.TrailingCharacter = ListTrailingCharacter.Space;
listLevel.NumberPosition = 144;

// Crea paragrafi e applica loro entrambi i livelli di elenco della nostra formattazione di elenco personalizzata.
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ListFormat.List = list;
builder.Writeln("The quick brown fox...");
builder.Writeln("The quick brown fox...");

builder.ListFormat.ListIndent();
builder.Writeln("jumped over the lazy dog.");
builder.Writeln("jumped over the lazy dog.");

builder.ListFormat.ListOutdent();
builder.Writeln("The quick brown fox...");

builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateCustomList.docx");
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

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)
