---
title: Shape.FirstParagraph
linktitle: FirstParagraph
articleTitle: FirstParagraph
second_title: Aspose.Words per .NET
description: Recupera il primo paragrafo di una forma senza sforzo. Migliora il layout del tuo documento con la nostra funzionalità "Forma PrimoParagrafo" di facile utilizzo.
type: docs
weight: 70
url: /it/net/aspose.words.drawing/shape/firstparagraph/
---
## Shape.FirstParagraph property

Ottiene il primo paragrafo nella forma.

```csharp
public Paragraph FirstParagraph { get; }
```

## Esempi

Mostra come creare e formattare una casella di testo.

```csharp
Document doc = new Document();

// Crea una casella di testo mobile.
Shape textBox = new Shape(doc, ShapeType.TextBox);
textBox.WrapType = WrapType.None;
textBox.Height = 50;
textBox.Width = 200;

// Imposta l'allineamento orizzontale e verticale del testo all'interno della forma.
textBox.HorizontalAlignment = HorizontalAlignment.Center;
textBox.VerticalAlignment = VerticalAlignment.Top;

// Aggiungere un paragrafo alla casella di testo e aggiungere una sequenza di testo che verrà visualizzata nella casella di testo.
textBox.AppendChild(new Paragraph(doc));
Paragraph para = textBox.FirstParagraph;
para.ParagraphFormat.Alignment = ParagraphAlignment.Center;
Run run = new Run(doc);
run.Text = "Hello world!";
para.AppendChild(run);

doc.FirstSection.Body.FirstParagraph.AppendChild(textBox);

doc.Save(ArtifactsDir + "Shape.CreateTextBox.docx");
```

### Guarda anche

* class [Paragraph](../../../aspose.words/paragraph/)
* class [Shape](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
