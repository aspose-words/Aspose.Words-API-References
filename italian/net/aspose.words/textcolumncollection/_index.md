---
title: Class TextColumnCollection
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TextColumnCollection classe. Una raccolta diTextColumn oggetti che rappresentano tutte le colonne di testo in una sezione di un documento.
type: docs
weight: 6100
url: /it/net/aspose.words/textcolumncollection/
---
## TextColumnCollection class

Una raccolta di[`TextColumn`](../textcolumn/) oggetti che rappresentano tutte le colonne di testo in una sezione di un documento.

```csharp
public class TextColumnCollection
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [Count](../../aspose.words/textcolumncollection/count/) { get; } | Ottiene il numero di colonne nella sezione di un documento. |
| [EvenlySpaced](../../aspose.words/textcolumncollection/evenlyspaced/) { get; set; } | **Vero** se le colonne di testo sono di uguale larghezza e spaziate uniformemente. |
| [Item](../../aspose.words/textcolumncollection/item/) { get; } | Restituisce una colonna di testo in corrispondenza dell'indice specificato. |
| [LineBetween](../../aspose.words/textcolumncollection/linebetween/) { get; set; } | Quando **VERO** , aggiunge una linea verticale tra le colonne. |
| [Spacing](../../aspose.words/textcolumncollection/spacing/) { get; set; } | Quando le colonne sono distanziate uniformemente, ottiene o imposta la quantità di spazio tra ciascuna colonna in punti. |
| [Width](../../aspose.words/textcolumncollection/width/) { get; } | Quando le colonne sono equidistanti, ottiene la larghezza delle colonne. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [SetCount](../../aspose.words/textcolumncollection/setcount/)(int) | Dispone il testo nel numero specificato di colonne di testo. |

### Osservazioni

Uso[`SetCount`](./setcount/) per impostare il numero di colonne di testo.

Per fare in modo che tutte le colonne abbiano la stessa larghezza e la spaziatura uniforme, impostare[`EvenlySpaced`](./evenlyspaced/) a **VERO** e specificare la quantità di spazio tra le colonne in[`Spacing`](./spacing/). MS Word calcolerà automaticamente le larghezze delle colonne.

Se hai **uniformemente distanziati** impostato **falso** è necessario specificare la larghezza e la spaziatura per ciascuna colonna individualmente. Utilizzare l'indicizzatore per accedere a individuo[`TextColumn`](../textcolumn/) oggetti.

Quando si utilizzano larghezze di colonna personalizzate, assicurarsi che la somma di tutte le larghezze e le spaziature delle colonne tra di esse sia uguale alla larghezza della pagina meno i margini della pagina sinistro e destro.

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


