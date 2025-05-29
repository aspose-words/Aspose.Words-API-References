---
title: ShapeBase.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words per .NET
description: Scopri la proprietà Font ShapeBase per un facile accesso alla formattazione dei font. Migliora i tuoi design con stili di testo personalizzabili e opzioni tipografiche uniche.
type: docs
weight: 190
url: /it/net/aspose.words.drawing/shapebase/font/
---
## ShapeBase.Font property

Fornisce l'accesso alla formattazione del carattere di questo oggetto.

```csharp
public Font Font { get; }
```

## Esempi

Mostra come inserire una casella di testo e impostare il carattere del suo contenuto.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.TextBox, 300, 50);
builder.MoveTo(shape.LastParagraph);
builder.Write("This text is inside the text box.");

// Imposta la proprietà "Nascosto" dell'oggetto "Font" della forma su "true" per nascondere la casella di testo alla vista
// e comprimere lo spazio che normalmente occuperebbe.
// Imposta la proprietà "Nascosto" dell'oggetto "Carattere" della forma su "false" per lasciare visibile la casella di testo.
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

* class [Font](../../../aspose.words/font/)
* class [ShapeBase](../)
* spazio dei nomi [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../../)
