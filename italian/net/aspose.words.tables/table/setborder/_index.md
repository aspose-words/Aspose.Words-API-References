---
title: Table.SetBorder
second_title: Aspose.Words per .NET API Reference
description: Table metodo. Imposta il bordo della tabella specificato sullo stile di linea sulla larghezza e sul colore specificati.
type: docs
weight: 410
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
| lineStyle | LineStyle | Lo stile della linea da applicare. |
| lineWidth | Double | La larghezza della linea da impostare (in punti). |
| color | Color | Il colore da usare per il bordo. |
| isOverrideCellBorders | Boolean | quando`VERO`, fa sì che tutti i bordi delle celle esplicite esistenti vengano rimossi. |

### Esempi

Mostra come applicare un bordo del contorno a una tabella.

```csharp
Document doc = new Document(MyDir + "Tables.docx");
Table table = doc.FirstSection.Body.Tables[0];

// Allinea la tabella al centro della pagina.
table.Alignment = TableAlignment.Center;

// Cancella i bordi e l'ombreggiatura esistenti dalla tabella.
table.ClearBorders();
table.ClearShading();

// Aggiungi bordi verdi al contorno della tabella.
table.SetBorder(BorderType.Left, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Right, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Top, LineStyle.Single, 1.5, Color.Green, true);
table.SetBorder(BorderType.Bottom, LineStyle.Single, 1.5, Color.Green, true);

// Riempi le celle con un colore solido verde chiaro.
table.SetShading(TextureIndex.TextureSolid, Color.LightGreen, Color.Empty);

doc.Save(ArtifactsDir + "Table.SetOutlineBorders.docx");
```

### Guarda anche

* enum [BorderType](../../../aspose.words/bordertype/)
* enum [LineStyle](../../../aspose.words/linestyle/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../table/)
* assemblea [Aspose.Words](../../../)


