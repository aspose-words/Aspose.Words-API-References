---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words per .NET
description: Table SetBorder metodo. Imposta il bordo della tabella specificato sullo stile di linea larghezza e colore specificati in C#.
type: docs
weight: 410
url: /it/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Imposta il bordo della tabella specificato sullo stile di linea, larghezza e colore specificati.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderType | BorderType | Il bordo della tabella da modificare. |
| lineStyle | LineStyle | Lo stile di linea da applicare. |
| lineWidth | Double | Lo spessore della linea da impostare (in punti). |
| color | Color | Il colore da utilizzare per il bordo. |
| isOverrideCellBorders | Boolean | Quando`VERO`, provoca la rimozione di tutti i bordi espliciti delle celle esistenti. |

## Esempi

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
