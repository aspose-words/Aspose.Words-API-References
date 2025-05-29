---
title: TextBoxAnchor Enum
linktitle: TextBoxAnchor
articleTitle: TextBoxAnchor
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Drawing.TextBoxAnchor per un allineamento verticale preciso del testo delle forme. Migliora la formattazione dei tuoi documenti senza sforzo!
type: docs
weight: 1740
url: /it/net/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enumeration

Specifica i valori utilizzati per l'allineamento verticale del testo della forma.

```csharp
public enum TextBoxAnchor
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Top | `0` | Il testo è allineato alla parte superiore della casella di testo. |
| Middle | `1` | Il testo è allineato al centro della casella di testo. |
| Bottom | `2` | Il testo è allineato alla parte inferiore della casella di testo. |
| TopCentered | `3` | Il testo è allineato al centro della parte superiore della casella di testo. |
| MiddleCentered | `4` | Il testo è allineato al centro della casella di testo. |
| BottomCentered | `5` | Il testo è allineato al centro della parte inferiore della casella di testo. |
| TopBaseline | `6` | Il testo è allineato alla linea di base superiore della casella di testo. |
| BottomBaseline | `7` | Il testo è allineato alla linea di base inferiore della casella di testo. |
| TopCenteredBaseline | `8` | Il testo è allineato alla linea di base centrata in alto della casella di testo. |
| BottomCenteredBaseline | `9` | Il testo è allineato alla linea di base centrata in basso della casella di testo. |

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

* spazio dei nomi [Aspose.Words.Drawing](../../aspose.words.drawing/)
* assemblea [Aspose.Words](../../)
