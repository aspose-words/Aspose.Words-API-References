---
title: Table.SetShading
linktitle: SetShading
articleTitle: SetShading
second_title: Aspose.Words per .NET
description: Table SetShading metodo. Imposta lombreggiatura sui valori specificati sullintera tabella in C#.
type: docs
weight: 430
url: /it/net/aspose.words.tables/table/setshading/
---
## Table.SetShading method

Imposta l'ombreggiatura sui valori specificati sull'intera tabella.

```csharp
public void SetShading(TextureIndex texture, Color foregroundColor, Color backgroundColor)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| texture | TextureIndex | La texture da applicare. |
| foregroundColor | Color | Il colore della trama. |
| backgroundColor | Color | Il colore del riempimento dello sfondo. |

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

* enum [TextureIndex](../../../aspose.words/textureindex/)
* class [Table](../)
* spazio dei nomi [Aspose.Words.Tables](../../../aspose.words.tables/)
* assemblea [Aspose.Words](../../../)
