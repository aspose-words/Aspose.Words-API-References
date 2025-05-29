---
title: TextBox.LayoutFlow
linktitle: LayoutFlow
articleTitle: LayoutFlow
second_title: Aspose.Words per .NET
description: Scopri come la proprietà TextBox LayoutFlow ottimizza il layout del testo nelle forme, migliorando la flessibilità di progettazione e la leggibilità dei tuoi progetti.
type: docs
weight: 60
url: /it/net/aspose.words.drawing/textbox/layoutflow/
---
## TextBox.LayoutFlow property

Determina il flusso del layout del testo in una forma.

```csharp
public LayoutFlow LayoutFlow { get; set; }
```

## Osservazioni

Il valore predefinito èHorizontal.

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

* enum [LayoutFlow](../../layoutflow/)
* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
