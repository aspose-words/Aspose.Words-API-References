---
title: List.IsMultiLevel
linktitle: IsMultiLevel
articleTitle: IsMultiLevel
second_title: Aspose.Words per .NET
description: Scopri se la tua lista supporta più livelli! Il nostro strumento rivela "vero" per 9 livelli e "falso" per 1, migliorando l'efficienza della gestione dei dati.
type: docs
weight: 40
url: /it/net/aspose.words.lists/list/ismultilevel/
---
## List.IsMultiLevel property

Restituisce`VERO` quando l'elenco contiene 9 livelli;`falso` quando 1 livello.

```csharp
public bool IsMultiLevel { get; }
```

## Osservazioni

Gli elenchi creati con Aspose.Words sono sempre elenchi multilivello e contengono 9 livelli.

Microsoft Word 2003 e versioni successive creano sempre elenchi multilivello con 9 livelli. Tuttavia, in alcuni documenti creati con versioni precedenti di Microsoft Word, potresti imbatterti in elenchi che hanno solo 1 livello.

## Esempi

Mostra come creare uno stile di elenco e utilizzarlo in un documento.

```csharp
Document doc = new Document();

// Un elenco ci consente di organizzare e decorare serie di paragrafi con simboli di prefisso e rientri.
 // Possiamo creare elenchi annidati aumentando il livello di rientro.
 // Possiamo iniziare e terminare un elenco utilizzando la proprietà "ListFormat" di un generatore di documenti.
// Ogni paragrafo che aggiungiamo tra l'inizio e la fine di un elenco diventerà un elemento dell'elenco.
// Possiamo contenere un intero oggetto List all'interno di uno stile.
Style listStyle = doc.Styles.Add(StyleType.List, "MyListStyle");

List list1 = listStyle.List;

Assert.True(list1.IsListStyleDefinition);
Assert.False(list1.IsListStyleReference);
Assert.True(list1.IsMultiLevel);
Assert.AreEqual(listStyle, list1.Style);

// Modifica l'aspetto di tutti i livelli dell'elenco.
foreach (ListLevel level in list1.ListLevels)
{
    level.Font.Name = "Verdana";
    level.Font.Color = Color.Blue;
    level.Font.Bold = true;
}

DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Using list style first time:");

// Crea un altro elenco da un elenco all'interno di uno stile.
List list2 = doc.Lists.Add(listStyle);

Assert.False(list2.IsListStyleDefinition);
Assert.True(list2.IsListStyleReference);
Assert.AreEqual(listStyle, list2.Style);

// Aggiungi alcuni elementi dell'elenco che verranno formattati dal nostro elenco.
builder.ListFormat.List = list2;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Writeln("Using list style second time:");

// Crea e applica un altro elenco in base allo stile dell'elenco.
List list3 = doc.Lists.Add(listStyle);
builder.ListFormat.List = list3;
builder.Writeln("Item 1");
builder.Writeln("Item 2");
builder.ListFormat.RemoveNumbers();

builder.Document.Save(ArtifactsDir + "Lists.CreateAndUseListStyle.docx");
```

### Guarda anche

* class [List](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
