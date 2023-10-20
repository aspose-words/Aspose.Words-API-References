---
title: ShapeBase.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words per .NET
description: ShapeBase Name proprietà. Ottiene o imposta il nome della forma opzionale in C#.
type: docs
weight: 400
url: /it/net/aspose.words.drawing/shapebase/name/
---
## ShapeBase.Name property

Ottiene o imposta il nome della forma opzionale.

```csharp
public string Name { get; set; }
```

## Osservazioni

L'impostazione predefinita è una stringa vuota.

Non può essere`nullo`, ma può essere una stringa vuota.

## Esempi

Mostra come utilizzare il testo alternativo di una forma.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Shape shape = builder.InsertShape(ShapeType.Cube, 150, 150);
shape.Name = "MyCube";

shape.AlternativeText = "Alt text for MyCube.";

// Possiamo accedere al testo alternativo di una forma facendo clic con il pulsante destro del mouse su di esso, quindi tramite "Formatta forma automatica" -> "Testo alternativo".
doc.Save(ArtifactsDir + "Shape.AltText.docx");

// Salva il documento in HTML, quindi elimina l'immagine collegata che appartiene alla nostra forma.
// Il browser che sta leggendo il nostro HTML visualizzerà il testo alternativo al posto dell'immagine mancante.
doc.Save(ArtifactsDir + "Shape.AltText.html");
File.Delete(ArtifactsDir + "Shape.AltText.001.png");
```

### Guarda anche

* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
