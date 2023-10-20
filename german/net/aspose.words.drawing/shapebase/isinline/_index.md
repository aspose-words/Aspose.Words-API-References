---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words für .NET
description: ShapeBase IsInline eigendom. Eine schnelle Möglichkeit festzustellen ob diese Form im Text positioniert ist in C#.
type: docs
weight: 290
url: /de/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Eine schnelle Möglichkeit, festzustellen, ob diese Form im Text positioniert ist.

```csharp
public bool IsInline { get; }
```

## Bemerkungen

Hat nur Auswirkungen auf Formen der obersten Ebene.

## Beispiele

Zeigt, wie Sie bestimmen, ob eine Form eingebunden oder schwebend ist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nachfolgend sind zwei Umhüllungstypen aufgeführt, die Formen haben können.
// 1 - Inline:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Eine Inline-Form befindet sich innerhalb eines Absatzes zwischen anderen Absatzelementen, z. B. Textläufen.
// In Microsoft Word können wir auf die Form klicken und sie in einen beliebigen Absatz ziehen, als wäre es ein Zeichen.
// Wenn die Form groß ist, wirkt sich dies auf den vertikalen Absatzabstand aus.
// Wir können diese Form nicht an eine Stelle ohne Absatz verschieben.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Floating:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Eine schwebende Form gehört zu dem Absatz, in den wir sie einfügen.
// was wir durch ein Ankersymbol erkennen können, das erscheint, wenn wir auf die Form klicken.
// Wenn die Form links kein sichtbares Ankersymbol hat,
// Wir müssen sichtbare Anker über „Optionen“ aktivieren -> „Anzeige“ -> „Objektanker“.
// In Microsoft Word können wir mit der linken Maustaste auf diese Form klicken und sie an eine beliebige Stelle ziehen.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
