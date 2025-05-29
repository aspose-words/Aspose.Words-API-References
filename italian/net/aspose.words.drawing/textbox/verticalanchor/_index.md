---
title: TextBox.VerticalAnchor
linktitle: VerticalAnchor
articleTitle: VerticalAnchor
second_title: Aspose.Words per .NET
description: Scopri come la proprietà TextBox VerticalAnchor migliora l'allineamento del testo all'interno delle forme, migliorando il design e la leggibilità dei tuoi progetti.
type: docs
weight: 120
url: /it/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Specifica l'allineamento verticale del testo all'interno di una forma.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

## Osservazioni

Il valore predefinito èTop.

## Esempi

Mostra come allineare verticalmente il contenuto di testo di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Top" per
// allinea il testo in questa casella di testo con il lato superiore della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Middle" per
// allinea il testo in questa casella di testo al centro della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Bottom" per
// allinea il testo in questa casella di testo alla parte inferiore della forma.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'allineamento verticale del testo all'interno delle caselle di testo è disponibile a partire da Microsoft Word 2007.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Guarda anche

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
