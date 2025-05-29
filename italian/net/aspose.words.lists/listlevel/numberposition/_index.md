---
title: ListLevel.NumberPosition
linktitle: NumberPosition
articleTitle: NumberPosition
second_title: Aspose.Words per .NET
description: Scopri la proprietà NumberPosition di ListLevel per regolare facilmente il posizionamento di punti elenco o numeri in punti, per una formattazione e una chiarezza migliorate degli elenchi.
type: docs
weight: 80
url: /it/net/aspose.words.lists/listlevel/numberposition/
---
## ListLevel.NumberPosition property

Restituisce o imposta la posizione (in punti) del numero o del punto elenco per il livello dell'elenco.

```csharp
public double NumberPosition { get; set; }
```

## Osservazioni

`NumberPosition` corrisponde a LeftIndent più FirstLineIndent del paragrafo.

## Esempi

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

### Guarda anche

* class [ListLevel](../)
* spazio dei nomi [Aspose.Words.Lists](../../../aspose.words.lists/)
* assemblea [Aspose.Words](../../../)
