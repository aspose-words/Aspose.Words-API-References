---
title: CellFormat.SetPaddings
linktitle: SetPaddings
articleTitle: SetPaddings
second_title: Aspose.Words per .NET
description: Scopri il metodo CellFormat SetPaddings per personalizzare la spaziatura delle celle in punti, ottimizzando il layout per una migliore leggibilità e un design migliore.
type: docs
weight: 170
url: /it/net/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat.SetPaddings method

Imposta la quantità di spazio (in punti) da aggiungere a sinistra/in alto/a destra/in basso al contenuto della cella.

```csharp
public void SetPaddings(double leftPadding, double topPadding, double rightPadding, 
    double bottomPadding)
```

## Esempi

Mostra come aggiungere spazi vuoti al contenuto di una cella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Imposta una distanza di riempimento (in punti) tra il bordo e il contenuto del testo
 // di ogni cella della tabella che creiamo con il generatore di documenti.
builder.CellFormat.SetPaddings(5, 10, 40, 50);

// Crea una tabella con una cella il cui contenuto avrà spazi vuoti.
builder.StartTable();
builder.InsertCell();
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. " +
              "Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc.Save(ArtifactsDir + "CellFormat.Padding.docx");
```

### Guarda anche

* class [CellFormat](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
