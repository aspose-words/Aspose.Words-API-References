---
title: ListTrailingCharacter Enum
linktitle: ListTrailingCharacter
articleTitle: ListTrailingCharacter
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Lists.ListTrailingCharacter per personalizzare le etichette degli elenchi e migliorare la formattazione dei paragrafi per una presentazione del documento impeccabile.
type: docs
weight: 3990
url: /it/net/aspose.words.lists/listtrailingcharacter/
---
## ListTrailingCharacter enumeration

Specifica il carattere che separa l'etichetta dell'elenco dal testo del paragrafo.

```csharp
public enum ListTrailingCharacter
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Tab | `0` | Un carattere di tabulazione viene inserito tra l'etichetta dell'elenco e il testo del paragrafo. |
| Space | `1` | Tra l'etichetta dell'elenco e il testo del paragrafo viene inserito uno spazio. |
| Nothing | `2` | Non c'è alcun carattere separatore tra l'etichetta dell'elenco e il testo del paragrafo. |

## Osservazioni

Utilizzato come valore per il[`TrailingCharacter`](../listlevel/trailingcharacter/) proprietà.

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
