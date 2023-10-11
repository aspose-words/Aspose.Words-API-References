---
title: TextBox.NoTextRotation
second_title: Aspose.Words per .NET API Reference
description: TextBox proprietà. Ottiene o imposta un valore booleano che indica che il testo del TextBox non deve ruotare quando viene ruotata la forma.
type: docs
weight: 80
url: /it/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Ottiene o imposta un valore booleano che indica che il testo del TextBox non deve ruotare quando viene ruotata la forma.

```csharp
public bool NoTextRotation { get; set; }
```

### Osservazioni

Il valore predefinito è`falso`

### Esempi

Mostra come disabilitare la rotazione del testo quando la forma viene ruotata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Guarda anche

* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../textbox/)
* assemblea [Aspose.Words](../../../)


