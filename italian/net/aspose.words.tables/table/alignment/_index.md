---
title: Table.Alignment
second_title: Aspose.Words per .NET API Reference
description: Table proprietà. Specifica come viene allineata una tabella in linea nel documento.
type: docs
weight: 40
url: /it/net/aspose.words.tables/table/alignment/
---
## Table.Alignment property

Specifica come viene allineata una tabella in linea nel documento.

```csharp
public TableAlignment Alignment { get; set; }
```

### Osservazioni

Il valore predefinito èLeft.

### Esempi

Mostra come applicare un bordo di contorno a una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Allinea la tabella al centro della pagina.
table.Alignment = TableAlignment.Center;

// Cancella eventuali bordi e ombreggiature esistenti dalla tabella.
table.ClearBorders();
table.ClearShading();

// Aggiunge bordi verdi al contorno della tabella.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Riempie le celle con un colore solido verde chiaro.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Guarda anche

* enum [TableAlignment](../../tablealignment/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


