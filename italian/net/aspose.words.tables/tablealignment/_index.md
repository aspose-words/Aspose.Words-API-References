---
title: Enum TableAlignment
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Tables.TableAlignment enum. Specifica lallineamento per una tabella inline.
type: docs
weight: 6050
url: /it/net/aspose.words.tables/tablealignment/
---
## TableAlignment enumeration

Specifica l'allineamento per una tabella inline.

```csharp
public enum TableAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Left | `0` | La tabella è allineata a sinistra. |
| Center | `1` | La tabella è centrata. |
| Right | `2` | La tabella è allineata a destra. |

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

* spazio dei nomi [Aspose.Words.Tables](../../aspose.words.tables/)
* assemblea [Aspose.Words](../../)


