---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words per .NET
description: Scopri la proprietà BackgroundShape di DocumentBase e personalizza facilmente la forma dello sfondo del tuo documento per un impatto visivo ancora maggiore. Sfrutta al massimo il tuo potenziale di design!
type: docs
weight: 10
url: /it/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Ottiene o imposta la forma dello sfondo del documento. Può essere`null` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Osservazioni

Microsoft Word consente solo una forma che ha il suo[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) proprietà equal aRectangle da utilizzare come forma di sfondo per un documento.

Microsoft Word supporta solo le proprietà di riempimento di una forma di sfondo. Tutte le altre proprietà vengono ignorate.

Impostando questa proprietà su un valore non nullo verrà anche impostata la[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) A`VERO`.

## Esempi

Mostra come impostare una forma di sfondo per ogni pagina di un documento.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// L'unico tipo di forma che possiamo usare come sfondo è un rettangolo.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Esistono due modi per utilizzare questa forma come sfondo di una pagina.
// 1 - Un colore piatto:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Un'immagine:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Regola l'aspetto dell'immagine per renderla più adatta come filigrana.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word non supporta forme con immagini come sfondi,
// ma possiamo comunque vedere questi sfondi in altri formati di salvataggio come .pdf.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Guarda anche

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
