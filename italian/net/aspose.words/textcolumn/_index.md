---
title: TextColumn Class
linktitle: TextColumn
articleTitle: TextColumn
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.TextColumn per gestire le colonne di testo nei tuoi documenti. Accedi e personalizza facilmente ogni colonna nella tua sezione di testo.
type: docs
weight: 7240
url: /it/net/aspose.words/textcolumn/
---
## TextColumn class

Rappresenta una singola colonna di testo.`TextColumn` è un membro del[`TextColumnCollection`](../textcolumncollection/) collezione. La`TextColumn`la raccolta include tutte le colonne in una sezione di un documento.

Per saperne di più, visita il[Lavorare con le sezioni](https://docs.aspose.com/words/net/working-with-sections/) articolo di documentazione.

```csharp
public class TextColumn
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [SpaceAfter](../../aspose.words/textcolumn/spaceafter/) { get; set; } | Ottiene o imposta lo spazio tra questa colonna e la colonna successiva in punti. Non richiesto per l'ultima colonna. |
| [Width](../../aspose.words/textcolumn/width/) { get; set; } | Ottiene o imposta la larghezza della colonna di testo in punti. |

## Osservazioni

`TextColumn` Gli oggetti vengono utilizzati solo per specificare colonne con larghezza e spaziatura personalizzate. Se si desidera che le colonne del documento abbiano la stessa larghezza, impostare TextColumns.[`EvenlySpaced`](../textcolumncollection/evenlyspaced/) A`VERO`.

Quando un nuovo`TextColumn` viene creato, la sua larghezza e la sua spaziatura sono impostate su zero.

## Esempi

Mostra come creare colonne con spaziature non uniformi.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
PageSetup pageSetup = builder.PageSetup;

TextColumnCollection columns = pageSetup.TextColumns;
columns.EvenlySpaced = false;
columns.SetCount(2);

// Determinare la quantità di spazio disponibile per disporre le colonne.
double contentWidth = pageSetup.PageWidth - pageSetup.LeftMargin - pageSetup.RightMargin;

Assert.AreEqual(470.30d, contentWidth, 0.01d);

// Imposta la prima colonna in modo che sia stretta.
TextColumn column = columns[0];
column.Width = 100;
column.SpaceAfter = 20;

// Imposta la seconda colonna in modo che occupi il resto dello spazio disponibile entro i margini della pagina.
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
