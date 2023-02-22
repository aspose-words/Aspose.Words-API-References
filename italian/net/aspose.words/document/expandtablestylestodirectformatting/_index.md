---
title: Document.ExpandTableStylesToDirectFormatting
second_title: Aspose.Words per .NET API Reference
description: Document metodo. Converte la formattazione specificata negli stili tabella nella formattazione diretta sulle tabelle nel documento.
type: docs
weight: 570
url: /it/net/aspose.words/document/expandtablestylestodirectformatting/
---
## Document.ExpandTableStylesToDirectFormatting method

Converte la formattazione specificata negli stili tabella nella formattazione diretta sulle tabelle nel documento.

```csharp
public void ExpandTableStylesToDirectFormatting()
```

### Osservazioni

Questo metodo esiste perché questa versione di Aspose.Words fornisce solo un supporto limitato per gli stili di tabella (vedi sotto). Questo metodo potrebbe essere utile quando carichi un documento DOCX o WordprocessingML che contiene tabelle formattate con stili di tabella e devi eseguire query sulla formattazione di tabelle, celle, paragrafi o testo di .

Questa versione di Aspose.Words fornisce un supporto limitato per gli stili di tabella come segue:

* Gli stili tabella definiti nei documenti DOCX o WordprocessingML vengono mantenuti come stili tabella quando si salva il documento come DOCX o WordprocessingML.
* Gli stili di tabella definiti nei documenti DOCX o WordprocessingML vengono automaticamente convertiti in formattazione diretta sulle tabelle quando si salva il documento in qualsiasi altro formato, rendering o stampa di .
* Gli stili di tabella definiti nei documenti DOC vengono mantenuti come stili di tabella quando si salva il documento solo come DOC.

### Esempi

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

// Questo metodo riguarda le proprietà dello stile della tabella come quelle impostate sopra.
doc.ExpandTableStylesToDirectFormatting();

doc.Save(ArtifactsDir + "Document.TableStyleToDirectFormatting.docx");
```

### Guarda anche

* class [Document](../)
* spazio dei nomi [Aspose.Words](../../document/)
* assemblea [Aspose.Words](../../../)


