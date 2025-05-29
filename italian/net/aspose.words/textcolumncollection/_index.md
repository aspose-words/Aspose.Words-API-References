---
title: TextColumnCollection Class
linktitle: TextColumnCollection
articleTitle: TextColumnCollection
second_title: Aspose.Words per .NET
description: Esplora Aspose.Words.TextColumnCollection per gestire le colonne di testo nei tuoi documenti senza sforzo. Migliora la formattazione dei tuoi documenti con facilità!
type: docs
weight: 7250
url: /it/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Una raccolta di[`TextColumn`](../textcolumn/) oggetti che rappresentano tutte le colonne di testo in una sezione di un documento.

Per saperne di più, visita il[Lavorare con le sezioni](https://docs.aspose.com/words/net/working-with-sections/) articolo di documentazione.

```csharp
public class TextColumnCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Ottiene il numero di colonne nella sezione di un documento. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Vero se le colonne di testo hanno la stessa larghezza e sono uniformemente distanziate. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Restituisce una colonna di testo all'indice specificato. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Quando`VERO` , aggiunge una linea verticale tra le colonne. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Quando le colonne sono distanziate uniformemente, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Quando le colonne sono distanziate uniformemente, ottiene la larghezza delle colonne. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(*int*) | Dispone il testo nel numero specificato di colonne di testo. |

## Osservazioni

Utilizzo[`SetCount`](./setcount/) per impostare il numero di colonne di testo.

Per rendere tutte le colonne di larghezza uguale e distanziate uniformemente, impostare[`EvenlySpaced`](./evenlyspaced/) A`VERO` e specificare la quantità di spazio tra le colonne in[`Spacing`](./spacing/)MS Word calcolerà automaticamente la larghezza delle colonne.

Se hai[`EvenlySpaced`](./evenlyspaced/) impostato su`falso` , è necessario specificare larghezza e spaziatura per ogni colonna individualmente. Utilizzare l'indicizzatore per accedere ai singoli[`TextColumn`](../textcolumn/) oggetti.

Quando si utilizzano larghezze di colonna personalizzate, assicurarsi che la somma di tutte le larghezze delle colonne e delle spaziature tra di esse sia uguale alla larghezza della pagina meno i margini sinistro e destro della pagina.

## Esempi

Mostra come creare più colonne equidistanti in una sezione.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

TextColumnCollection columns = builder.PageSetup.TextColumns;
columns.Spacing = 100;
columns.SetCount(2);

builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

doc.Save(ArtifactsDir + "PageSetup.ColumnsSameWidth.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
