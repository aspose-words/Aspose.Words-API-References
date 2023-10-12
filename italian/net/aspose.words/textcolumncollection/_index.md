---
title: Class TextColumnCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TextColumnCollection classe. Una raccolta diTextColumn oggetti che rappresentano tutte le colonne di testo in una sezione di un documento.
type: docs
weight: 6400
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
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | Vero se le colonne di testo hanno la stessa larghezza e spaziate uniformemente. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Restituisce una colonna di testo nell'indice specificato. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Quando`VERO` aggiunge una linea verticale tra le colonne. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Quando le colonne sono distanziate uniformemente, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Quando le colonne sono spaziate uniformemente, ottiene la larghezza delle colonne. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(int) | Dispone il testo nel numero specificato di colonne di testo. |

### Osservazioni

Utilizzo[`SetCount`](./setcount/) per impostare il numero di colonne di testo.

Per fare in modo che tutte le colonne abbiano la stessa larghezza e una spaziatura uniforme, impostare[`EvenlySpaced`](./evenlyspaced/) A`VERO` e specifica la quantità di spazio tra le colonne in[`Spacing`](./spacing/). MS Word calcolerà automaticamente la larghezza delle colonne.

Se hai[`EvenlySpaced`](./evenlyspaced/) impostato`falso` , devi specificare la larghezza e la spaziatura per ciascuna colonna individualmente. Utilizzare l'indicizzatore per accedere ai singoli[`TextColumn`](../textcolumn/) oggetti.

Quando utilizzi larghezze di colonna personalizzate, assicurati che la somma di tutte le larghezze delle colonne e degli spazi tra loro sia uguale alla larghezza della pagina meno i margini sinistro e destro della pagina.

### Esempi

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


