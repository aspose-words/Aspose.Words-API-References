---
title: List.IsListStyleDefinition
linktitle: IsListStyleDefinition
articleTitle: IsListStyleDefinition
second_title: Aspose.Words per .NET
description: Scopri se la proprietà List IsListStyleDefinition definisce uno stile di elenco. Sblocca subito opzioni di stile avanzate per i tuoi elenchi!
type: docs
weight: 20
url: /it/net/aspose.words.lists/list/isliststyledefinition/
---
## List.IsListStyleDefinition property

Restituisce`VERO` se questo elenco è una definizione di uno stile di elenco.

```csharp
public bool IsListStyleDefinition { get; }
```

## Osservazioni

Quando questa proprietà è`VERO` , IL[`Style`](../style/) La proprietà restituisce lo stile di elenco definito da questo elenco.

Modificando le proprietà di un elenco che definisce uno stile di elenco, si modificano le proprietà dello stile di elenco.

Un elenco che è una definizione di uno stile di elenco non può essere applicato direttamente ai paragrafi per renderli numerati.

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
