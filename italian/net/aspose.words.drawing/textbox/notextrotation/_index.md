---
title: TextBox.NoTextRotation
linktitle: NoTextRotation
articleTitle: NoTextRotation
second_title: Aspose.Words per .NET
description: Controlla la rotazione del testo nella tua TextBox con la proprietà NoTextRotation. Garantisci un testo chiaro e leggibile anche quando le forme vengono ruotate. Migliora il tuo design!
type: docs
weight: 80
url: /it/net/aspose.words.drawing/textbox/notextrotation/
---
## TextBox.NoTextRotation property

Ottiene o imposta un valore booleano che indica che il testo della TextBox non deve ruotare quando la forma viene ruotata.

```csharp
public bool NoTextRotation { get; set; }
```

## Osservazioni

Il valore predefinito è`falso`

## Esempi

Mostra come disattivare la rotazione del testo quando la forma viene ruotata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Ellipse, 20, 20);
shape.TextBox.NoTextRotation = true;

doc.Save(ArtifactsDir + "Shape.NoTextRotation.docx");
```

### Guarda anche

* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
