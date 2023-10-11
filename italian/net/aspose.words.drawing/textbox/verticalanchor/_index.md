---
title: TextBox.VerticalAnchor
second_title: Aspose.Words per .NET API Reference
description: TextBox proprietà. Specifica lallineamento verticale del testo allinterno di una forma.
type: docs
weight: 120
url: /it/net/aspose.words.drawing/textbox/verticalanchor/
---
## TextBox.VerticalAnchor property

Specifica l'allineamento verticale del testo all'interno di una forma.

```csharp
public TextBoxAnchor VerticalAnchor { get; set; }
```

### Osservazioni

Il valore predefinito èTop.

### Esempi

Mostra come allineare verticalmente il contenuto del testo di una casella di testo.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.TextBox, 200, 200);

// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Top" su
// allinea il testo in questa casella di testo con il lato superiore della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Middle" su
// allinea il testo in questa casella di testo al centro della forma.
// Imposta la proprietà "VerticalAnchor" su "TextBoxAnchor.Bottom" su
// allinea il testo in questa casella di testo alla parte inferiore della forma.
shape.TextBox.VerticalAnchor = verticalAnchor;

builder.MoveTo(shape.FirstParagraph);
builder.Write("Hello world!");

// L'allineamento verticale del testo all'interno delle caselle di testo è disponibile da Microsoft Word 2007 in poi.
doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2007);
doc.Save(ArtifactsDir + "Shape.VerticalAnchor.docx");
```

### Guarda anche

* enum [TextBoxAnchor](../../textboxanchor/)
* class [TextBox](../)
* spazio dei nomi [Aspose.Words.Drawing](../../textbox/)
* assemblea [Aspose.Words](../../../)


