---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words per .NET
description: Aspose.Words.Drawing.RelativeVerticalPosition enum. Specifica a cosa è relativa la posizione verticale di una forma o di una cornice di testo in C#.
type: docs
weight: 1210
url: /it/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Specifica a cosa è relativa la posizione verticale di una forma o di una cornice di testo.

```csharp
public enum RelativeVerticalPosition
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Margin | `0` | Specifica che il posizionamento verticale sarà relativo ai margini della pagina. |
| Page | `1` | L'oggetto è posizionato rispetto al bordo superiore della pagina. |
| Paragraph | `2` | L'oggetto è posizionato rispetto alla parte superiore del paragrafo che contiene l'ancora. |
| Line | `3` | Non documentato. |
| TopMargin | `4` | Specifica che il posizionamento verticale sarà relativo al margine superiore della pagina corrente. |
| BottomMargin | `5` | Specifica che il posizionamento verticale sarà relativo al margine inferiore della pagina corrente. |
| InsideMargin | `6` | Specifica che il posizionamento verticale sarà relativo al margine interno della pagina corrente. |
| OutsideMargin | `7` | Specifica che il posizionamento verticale sarà relativo al margine esterno della pagina corrente. |
| TableDefault | `0` | Il valore predefinito èMargin . |
| TextFrameDefault | `2` | Il valore predefinito èParagraph . |

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
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Posiziona l'immagine al centro della pagina.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Mostra come inserire un'immagine e utilizzarla come filigrana (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisci l'immagine nell'intestazione in modo che sia visibile su ogni pagina.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Posiziona l'immagine al centro della pagina.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Guarda anche

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
