---
title: ShapeBase.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words per .NET
description: Scopri la proprietà ShapeBase RelativeVerticalPosition per migliorare l'allineamento verticale delle forme, assicurando un controllo preciso del layout nei tuoi progetti.
type: docs
weight: 470
url: /it/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Specifica in relazione a cosa è posizionata verticalmente la forma.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

## Osservazioni

Il valore predefinito èParagraph.

Ha effetto solo sulle forme mobili di livello superiore.

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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
