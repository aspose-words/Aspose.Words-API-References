---
title: Document.ExpandTableStylesToDirectFormatting
linktitle: ExpandTableStylesToDirectFormatting
articleTitle: ExpandTableStylesToDirectFormatting
second_title: Aspose.Words per .NET
description: Trasforma gli stili di tabella in formattazione diretta con il metodo ExpandTableStylesToDirectFormatting, migliorando senza sforzo l'aspetto del tuo documento.
type: docs
weight: 630
url: /it/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Converte la formattazione specificata negli stili di tabella in formattazione diretta sulle tabelle nel documento.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

## Osservazioni

Questo metodo esiste perché questa versione di Aspose.Words offre solo un supporto limitato per gli stili di tabella (vedi sotto). Questo metodo potrebbe essere utile quando si carica un documento DOCX o WordprocessingML contenente tabelle formattate con stili di tabella e si ha bisogno di interrogare la formattazione di tabelle, celle, paragrafi o testo .

Questa versione di Aspose.Words fornisce un supporto limitato per gli stili di tabella come segue:

* Gli stili di tabella definiti nei documenti DOCX o WordprocessingML vengono mantenuti come stili di tabella quando si salva il documento come DOCX o WordprocessingML.
* Gli stili di tabella definiti nei documenti DOCX o WordprocessingML vengono convertiti automaticamente in formattazione diretta sulle tabelle quando si salva il documento in qualsiasi altro formato, durante il rendering o la stampa.
* Gli stili di tabella definiti nei documenti DOC vengono mantenuti come stili di tabella solo quando si salva il documento come DOC.

## Esempi

Mostra come applicare le proprietà dello stile di una tabella direttamente agli elementi della tabella.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Hello world!");
builder.EndTable();

TableStyle tableStyle = (TableStyle)doc.Styles.Add(StyleType.Table, "MyTableStyle1");
tableStyle.RowStripe = 3;
tableStyle.CellSpacing = 5;
tableStyle.Shading.BackgroundPatternColor = Color.AntiqueWhite;
tableStyle.Borders.Color = Color.Blue;
tableStyle.Borders.LineStyle = LineStyle.DotDash;

table.Style = tableStyle;

// Questo metodo riguarda le proprietà di stile della tabella come quelle che abbiamo impostato sopra.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
