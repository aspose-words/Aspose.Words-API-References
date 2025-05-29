---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.RelativeHorizontalPosition per definire il posizionamento orizzontale preciso di forme e cornici di testo nei tuoi documenti.
type: docs
weight: 1580
url: /it/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Specifica a cosa è relativa la posizione orizzontale di una forma o di una cornice di testo.

```csharp
public enum RelativeHorizontalPosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Margin | `0` | Specifica che il posizionamento orizzontale deve essere relativo ai margini della pagina. |
| Page | `1` | L'oggetto è posizionato rispetto al bordo sinistro della pagina. |
| Column | `2` | L'oggetto è posizionato rispetto al lato sinistro della colonna. |
| Character | `3` | L'oggetto è posizionato rispetto al lato sinistro del paragrafo. |
| LeftMargin | `4` | Specifica che il posizionamento orizzontale deve essere relativo al margine sinistro della pagina. |
| RightMargin | `5` | Specifica che il posizionamento orizzontale deve essere relativo al margine destro della pagina. |
| InsideMargin | `6` | Specifica che il posizionamento orizzontale deve essere relativo al margine interno della pagina corrente (il margine sinistro sulle pagine dispari, quello destro sulle pagine pari). |
| OutsideMargin | `7` | Specifica che il posizionamento orizzontale deve essere relativo al margine esterno della pagina corrente (il margine destro sulle pagine dispari, quello sinistro sulle pagine pari). |
| Default | `2` | Il valore predefinito èColumn . |

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

Mostra come inserire un'immagine e utilizzarla come filigrana.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Posiziona l'immagine al centro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Guarda anche

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
