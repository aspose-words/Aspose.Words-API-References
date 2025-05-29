---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words per .NET
description: Scopri come l'enum Aspose.Words.Drawing.WrapType migliora l'adattamento del testo a forme e immagini per una formattazione professionale dei documenti.
type: docs
weight: 1810
url: /it/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Specifica come il testo viene disposto attorno a una forma o a un'immagine.

```csharp
public enum WrapType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| None | `3` | Nessun testo attorno alla forma. La forma è posizionata dietro o davanti al testo. |
| Inline | `0` | La forma rimane sullo stesso livello del testo e viene trattata come un carattere. |
| TopBottom | `1` | Il testo si interrompe nella parte superiore della forma e riprende sulla riga sottostante. |
| Square | `2` | Avvolge il testo attorno a tutti i lati del riquadro quadrato di delimitazione della forma. |
| Tight | `4` | Si avvolge strettamente attorno ai bordi della forma, invece di avvolgersi attorno al riquadro di delimitazione. |
| Through | `5` | Uguale a Tight, ma avvolge tutte le parti della forma che sono aperte. |

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

* property [WrapType](../shapebase/wraptype/)
* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
