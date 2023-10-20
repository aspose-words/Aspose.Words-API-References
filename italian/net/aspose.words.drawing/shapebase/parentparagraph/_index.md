---
title: ShapeBase.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words per .NET
description: ShapeBase ParentParagraph proprietà. Restituisce il paragrafo principale immediato in C#.
type: docs
weight: 410
url: /it/net/aspose.words.drawing/shapebase/parentparagraph/
---
## ShapeBase.ParentParagraph property

Restituisce il paragrafo principale immediato.

```csharp
public Paragraph ParentParagraph { get; }
```

## Osservazioni

Per le forme secondarie di una forma di gruppo e le forme secondarie di un oggetto Office Math restituisce sempre`nullo`.

## Esempi

Mostra come inserire una casella di testo e impostare il carattere del suo contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Imposta la proprietà "Hidden" dell'oggetto "Font" della forma su "true" per nascondere la casella di testo alla vista
// e comprime lo spazio che normalmente occuperebbe.
// Imposta la proprietà "Nascosto" dell'oggetto "Font" della forma su "false" per lasciare visibile la casella di testo.
shape.Font.Hidden = hideShape;

// Se la forma è visibile, ne modificheremo l'aspetto tramite l'oggetto font.
if (!hideShape)
{
    shape.Font.HighlightColor = Color.LightGray;
    shape.Font.Color = Color.Red;
    shape.Font.Underline = Underline.Dash;
}

// Sposta il builder fuori dalla casella di testo e riportalo nel documento principale.
builder.MoveTo(shape.ParentParagraph);

builder.Writeln("\nThis text is outside the text box.");

doc.Save(ArtifactsDir + "Shape.Font.docx");
```

### Guarda anche

* class [Paragraph](../../../aspose.words/paragraph/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
