---
title: Shape.TextBox
linktitle: TextBox
articleTitle: TextBox
second_title: Aspose.Words per .NET
description: Personalizza le proprietà della tua Shape TextBox per migliorare la visualizzazione del testo e l'aspetto dei tuoi progetti. Scatena la tua creatività oggi stesso!
type: docs
weight: 230
url: /it/net/aspose.words.drawing/shape/textbox/
---
## Shape.TextBox property

Definisce gli attributi che specificano come viene visualizzato il testo in una forma.

```csharp
public TextBox TextBox { get; }
```

## Esempi

Mostra come impostare l'orientamento del testo all'interno di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 150, 100);
TextBox textBox = textBoxShape.TextBox;

// Sposta il generatore di documenti all'interno della TextBox e aggiungi il testo.
builder.MoveTo(textBoxShape.LastParagraph);
builder.Writeln("Hello world!");
builder.Write("Hello again!");

// Imposta la proprietà "LayoutFlow" per impostare un orientamento per il contenuto di testo di questa casella di testo.
textBox.LayoutFlow = layoutFlow;

doc.Save(ArtifactsDir + "Shape.TextBoxLayoutFlow.docx");
```

### Guarda anche

* class [TextBox](../../textbox/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
