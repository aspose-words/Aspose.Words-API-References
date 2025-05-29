---
title: ListLevelAlignment Enum
linktitle: ListLevelAlignment
articleTitle: ListLevelAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Lists.ListLevelAlignment per un allineamento ottimale dei numeri e dei punti elenco. Migliora la formattazione dei documenti senza sforzo!
type: docs
weight: 3960
url: /it/net/aspose.words.lists/listlevelalignment/
---
## ListLevelAlignment enumeration

Specifica l'allineamento per il numero dell'elenco o il punto elenco.

```csharp
public enum ListLevelAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Left | `0` | L'etichetta dell'elenco è allineata a sinistra della posizione del numero. |
| Center | `1` | L'etichetta dell'elenco è centrata sulla posizione del numero. |
| Right | `2` | Questa etichetta di elenco è allineata a destra della posizione del numero. |

## Osservazioni

Utilizzato come valore per il[`Alignment`](../listlevel/alignment/) proprietà.

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

* spazio dei nomi [Aspose.Words.Lists](../../aspose.words.lists/)
* assemblea [Aspose.Words](../../)
