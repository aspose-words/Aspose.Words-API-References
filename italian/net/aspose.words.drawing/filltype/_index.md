---
title: FillType Enum
linktitle: FillType
articleTitle: FillType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.FillType per migliorare i tuoi oggetti compilabili con tipi di riempimento versatili per una migliore progettazione dei documenti.
type: docs
weight: 1280
url: /it/net/aspose.words.drawing/filltype/
---
## FillType enumeration

Specifica il tipo di riempimento per un oggetto riempibile.

```csharp
public enum FillType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Solid | `1` | Riempimento solido. |
| Patterned | `2` | Riempimento a motivi. |
| Gradient | `3` | Riempimento sfumato. |
| Textured | `4` | Riempimento strutturato. |
| Background | `5` | Il riempimento è uguale allo sfondo. |
| Picture | `6` | Riempimento immagine. |

## Esempi

Mostra come riconvertire uno qualsiasi dei riempimenti in riempimento uniforme.

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// Ottieni l'oggetto Fill per il font della prima esecuzione.
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// Controlla le proprietà di riempimento del font.
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// Cambia il tipo di riempimento in Solido con colore verde uniforme.
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
