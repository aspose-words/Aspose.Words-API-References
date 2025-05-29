---
title: Shape.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: Aspose.Words per .NET
description: Accedi alla proprietà LastParagraph per recuperare facilmente il paragrafo finale nel tuo formato, migliorando il layout e la leggibilità del tuo documento.
type: docs
weight: 130
url: /it/net/aspose.words.drawing/shape/lastparagraph/
---
## Shape.LastParagraph property

Ottiene l'ultimo paragrafo nella forma.

```csharp
public Paragraph LastParagraph { get; }
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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
