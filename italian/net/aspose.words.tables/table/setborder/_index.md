---
title: Table.SetBorder
linktitle: SetBorder
articleTitle: SetBorder
second_title: Aspose.Words per .NET
description: Personalizza l'aspetto della tua tabella con il metodo SetBorder: regola lo stile, la larghezza e il colore delle linee per un aspetto professionale. Migliora il tuo design oggi stesso!
type: docs
weight: 430
url: /it/net/aspose.words.tables/table/setborder/
---
## Table.SetBorder method

Imposta il bordo della tabella specificato sullo stile di linea, sulla larghezza e sul colore specificati.

```csharp
public void SetBorder(BorderType borderType, LineStyle lineStyle, double lineWidth, Color color, 
    bool isOverrideCellBorders)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| borderType | BorderType | Il bordo della tabella da modificare. |
| lineStyle | LineStyle | Stile della linea da applicare. |
| lineWidth | Double | Larghezza della linea da impostare (in punti). |
| color | Color | Il colore da usare per il bordo. |
| isOverrideCellBorders | Boolean | Quando`VERO`, fa sì che tutti i bordi espliciti delle celle esistenti vengano rimossi. |

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

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
