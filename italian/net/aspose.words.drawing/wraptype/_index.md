---
title: Enum WrapType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Drawing.WrapType enum. Specifica il modo in cui il testo viene disposto attorno a una forma o immagine.
type: docs
weight: 1400
url: /it/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Specifica il modo in cui il testo viene disposto attorno a una forma o immagine.

```csharp
public enum WrapType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `3` | Nessun testo attorno alla forma. La forma viene posizionata dietro o davanti al testo. |
| Inline | `0` | La forma rimane sullo stesso livello del testo e viene trattata come un carattere. |
| TopBottom | `1` | Il testo si ferma nella parte superiore della forma e ricomincia dalla riga sotto la forma. |
| Square | `2` | Avvolge il testo attorno a tutti i lati del riquadro di delimitazione quadrato della forma. |
| Tight | `4` | Avvolge strettamente i bordi della forma, invece di avvolgere il riquadro di delimitazione. |
| Through | `5` | Uguale a Stretto, ma avvolge tutte le parti della forma aperte. |

### Esempi

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

* property [WrapType](../shapebase/wraptype/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)


