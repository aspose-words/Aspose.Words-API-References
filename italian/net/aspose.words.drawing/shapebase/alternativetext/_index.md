---
title: ShapeBase.AlternativeText
second_title: Aspose.Words per .NET API Reference
description: ShapeBase proprietà. Definisce il testo alternativo da visualizzare al posto dellimmagine.
type: docs
weight: 20
url: /it/net/aspose.words.drawing/shapebase/alternativetext/
---
## ShapeBase.AlternativeText property

Definisce il testo alternativo da visualizzare al posto dell'immagine.

```csharp
public string AlternativeText { get; set; }
```

### Osservazioni

Il valore predefinito è una stringa vuota.

### Esempi

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
* spazio dei nomi [Aspose.Words.Drawing](../../shapebase/)
* assemblea [Aspose.Words](../../../)


