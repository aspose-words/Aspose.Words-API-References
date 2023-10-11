---
title: Class TextColumn
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.TextColumn classe. Rappresenta una singola colonna di testo.TextColumn è un membro delTextColumnCollection collezione. IlTextColumn la raccolta include tutte le colonne in una sezione di un documento.
type: docs
weight: 6390
url: /it/net/aspose.words/textcolumn/
---
## TextColumn class

Rappresenta una singola colonna di testo.`TextColumn` è un membro del[`TextColumnCollection`](../textcolumncollection/) collezione. Il`TextColumn` la raccolta include tutte le colonne in una sezione di un documento.

Per saperne di più, visita il[Lavorare con le sezioni](https://docs.aspose.com/words/net/working-with-sections/) articolo di documentazione.

```csharp
public class TextColumn
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Ottiene o imposta lo spazio tra questa colonna e la colonna successiva in punti. Non richiesto per l'ultima colonna. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Ottiene o imposta la larghezza della colonna di testo in punti. |

### Osservazioni

`TextColumn` gli oggetti vengono utilizzati solo per specificare colonne con larghezza e spaziatura personalizzate. Se vuoi che le colonne nel documento abbiano la stessa larghezza, imposta TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) A`VERO`.

Quando un nuovo`TextColumn` viene creato, ha la larghezza e la spaziatura impostate su zero.

### Esempi

Mostra come creare colonne con spaziatura non uniforme.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Determina la quantità di spazio disponibile per la disposizione delle colonne.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Imposta la prima colonna in modo che sia stretta.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Imposta la seconda colonna per occupare il resto dello spazio disponibile entro i margini della pagina.
column = columns[1];
column.Width = contentWidth - column.Width - column.SpaceAfter;

builder.Writeln("Narrow column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Wide column 2.");

doc.Save(ArtifactsDir + "PageSetup.CustomColumnWidth.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


