---
title: VerticalAlignment Enum
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.VerticalAlignment per un allineamento verticale preciso di cornici di testo e tabelle nei tuoi documenti. Migliora il controllo del layout!
type: docs
weight: 1790
url: /it/net/aspose.words.drawing/verticalalignment/
---
## VerticalAlignment enumeration

Specifica l'allineamento verticale di una forma mobile, di una cornice di testo o di una tabella mobile.

```csharp
public enum VerticalAlignment
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `0` | L'oggetto è posizionato in modo esplicito, solitamente utilizzando il suo**Superiore** proprietà. |
| Top | `1` | Specifica che l'oggetto deve trovarsi nella parte superiore della base di allineamento verticale. |
| Center | `2` | Specifica che l'oggetto deve essere centrato rispetto alla base di allineamento verticale. |
| Bottom | `3` | Specifica che l'oggetto deve trovarsi nella parte inferiore della base di allineamento verticale. |
| Inside | `4` | Specifica che l'oggetto deve essere all'interno della base di allineamento orizzontale. |
| Outside | `5` | Specifica che l'oggetto deve essere al di fuori della base di allineamento verticale. |
| Inline | `-1` | Non documentato. Sembra essere un valore possibile per paragrafi e tabelle mobili. |
| Default | `0` | Lo stesso diNone . |

## Esempi

Mostra come inserire un'immagine mobile al centro di una pagina.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci un'immagine mobile che apparirà dietro il testo sovrapposto e allineala al centro della pagina.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

### Guarda anche

* property [VerticalAlignment](../shapebase/verticalalignment/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
