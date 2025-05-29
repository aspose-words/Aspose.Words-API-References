---
title: Table.AllowAutoFit
linktitle: AllowAutoFit
articleTitle: AllowAutoFit
second_title: Aspose.Words per .NET
description: Scopri la proprietà Table AllowAutoFit per ridimensionare senza sforzo le celle delle tabelle di Microsoft Word e Aspose.Words, migliorando la leggibilità e la presentazione del tuo documento.
type: docs
weight: 50
url: /it/net/aspose.words.tables/table/allowautofit/
---
## Table.AllowAutoFit property

Consente a Microsoft Word e Aspose.Words di ridimensionare automaticamente le celle di una tabella per adattarle al loro contenuto.

```csharp
public bool AllowAutoFit { get; set; }
```

## Osservazioni

Il valore predefinito è`VERO`.

## Esempi

Mostra come abilitare/disabilitare il ridimensionamento automatico delle celle della tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.FromPoints(100);
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

builder.InsertCell();
builder.CellFormat.PreferredWidth = PreferredWidth.Auto;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
              "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");
builder.EndRow();
builder.EndTable();

// Imposta la proprietà "AllowAutoFit" su "false" per far sì che la tabella mantenga le dimensioni
// di tutte le sue righe e celle e tronca il contenuto se diventa troppo grande per essere inserito.
// Imposta la proprietà "AllowAutoFit" su "true" per consentire alla tabella di modificare la larghezza e l'altezza delle sue celle
// per ospitare il loro contenuto.
table.AllowAutoFit = allowAutoFit;

doc.Save(ArtifactsDir + "Table.AllowAutoFitOnTable.html");
```

### Guarda anche

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
