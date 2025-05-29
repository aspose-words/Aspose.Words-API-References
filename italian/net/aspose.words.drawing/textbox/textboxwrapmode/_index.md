---
title: TextBox.TextBoxWrapMode
linktitle: TextBoxWrapMode
articleTitle: TextBoxWrapMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextBox WrapMode per migliorare l'avvolgimento del testo nelle forme, migliorando la chiarezza e l'attrattiva visiva del tuo design.
type: docs
weight: 110
url: /it/net/aspose.words.drawing/textbox/textboxwrapmode/
---
## TextBox.TextBoxWrapMode property

Determina come il testo viene disposto all'interno di una forma.

```csharp
public TextBoxWrapMode TextBoxWrapMode { get; set; }
```

## Osservazioni

Il valore predefinito èSquare.

## Esempi

Mostra come impostare una modalità di avvolgimento per il contenuto di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape textBoxShape = builder.InsertShape(ShapeType.TextBox, 300, 300);
TextBox textBox = textBoxShape.TextBox;

// Imposta la proprietà "TextBoxWrapMode" su "TextBoxWrapMode.None" per aumentare la larghezza della casella di testo
// per contenere il testo, se sufficientemente grande.
// Imposta la proprietà "TextBoxWrapMode" su "TextBoxWrapMode.Square" per
// racchiude tutto il testo all'interno della casella di testo, mantenendone le dimensioni.
textBox.TextBoxWrapMode = textBoxWrapMode;

builder.MoveTo(textBoxShape.LastParagraph);
builder.Font.Size = 32;
builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.Save(ArtifactsDir + "Shape.TextBoxContentsWrapMode.docx");
```

### Guarda anche

* enum [TextBoxWrapMode](../../textboxwrapmode/)
* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
