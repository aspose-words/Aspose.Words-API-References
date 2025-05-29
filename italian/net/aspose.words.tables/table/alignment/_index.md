---
title: Table.Alignment
linktitle: Alignment
articleTitle: Alignment
second_title: Aspose.Words per .NET
description: Scopri la proprietà Allineamento tabella per controllare senza sforzo il posizionamento delle tabelle in linea nei tuoi documenti, ottenendo un aspetto curato e professionale.
type: docs
weight: 40
url: /it/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Specifica come una tabella in linea viene allineata nel documento.

```csharp
public TableAlignment Alignment { get; set; }
```

## Osservazioni

Il valore predefinito èLeft.

## Esempi

Mostra come applicare un bordo di contorno a una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Allinea la tabella al centro della pagina.
table.Alignment = TableAlignment.Center;

// Cancella tutti i bordi e le ombreggiature esistenti dalla tabella.
table.ClearBorders();
table.ClearShading();

// Aggiungere bordi verdi al contorno della tabella.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Riempi le celle con un colore verde chiaro uniforme.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Guarda anche

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
