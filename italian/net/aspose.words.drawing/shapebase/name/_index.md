---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: Scopri la proprietà Nome ShapeBase per gestire facilmente i nomi delle forme opzionali, migliorando la flessibilità di progettazione e l'organizzazione del progetto.
type: docs
weight: 420
url: /it/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Ottiene o imposta il nome facoltativo della forma.

```csharp
public string Name { get; set; }
```

## Osservazioni

Il valore predefinito è una stringa vuota.

Non può essere`null`, ma può essere una stringa vuota.

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
