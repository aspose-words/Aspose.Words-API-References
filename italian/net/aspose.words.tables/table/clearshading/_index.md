---
title: Table.ClearShading
linktitle: ClearShading
articleTitle: ClearShading
second_title: Aspose.Words per .NET
description: Scopri il metodo Table ClearShading per eliminare senza sforzo le ombreggiature delle tabelle, migliorando la chiarezza e la presentazione dei tuoi progetti.
type: docs
weight: 400
url: /it/net/aspose.words.tables/table/clearshading/
---
## Table.ClearShading method

Rimuove tutte le ombreggiature sulla tabella.

```csharp
public void ClearShading()
```

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

* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
