---
title: ShapeBase.AlternativeText
linktitle: AlternativeText
articleTitle: AlternativeText
second_title: Aspose.Words per .NET
description: Scopri la proprietà AlternativeText di ShapeBase, che migliora l'accessibilità fornendo testo descrittivo per la grafica, migliorando l'esperienza utente e la SEO.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Definisce il testo alternativo da visualizzare al posto di un'immagine.

```csharp
public string AlternativeText { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

## Esempi

Mostra come utilizzare il testo alternativo di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Possiamo accedere al testo alternativo di una forma cliccandoci sopra con il tasto destro del mouse e poi selezionando "Formato forma automatica" -> "Testo alternativo".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Salviamo il documento in formato HTML, quindi eliminiamo l'immagine collegata che appartiene alla nostra forma.
// Il browser che legge il nostro HTML visualizzerà il testo alt al posto dell'immagine mancante.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
