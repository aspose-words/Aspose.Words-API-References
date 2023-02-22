---
title: ShapeBase.IsInline
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Eine schnelle Möglichkeit festzustellen ob diese Form inline mit Text positioniert ist.
type: docs
weight: 280
url: /de/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Eine schnelle Möglichkeit festzustellen, ob diese Form inline mit Text positioniert ist.

```csharp
public bool IsInline { get; }
```

### Bemerkungen

Hat nur Auswirkungen auf Shapes der obersten Ebene.

### Beispiele

Zeigt, wie bestimmt wird, ob eine Form inline oder schwebend ist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Wrapping-Typen, die Shapes haben können.
// 1 - Inline:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Eine Inline-Form befindet sich innerhalb eines Absatzes zwischen anderen Absatzelementen, z. B. Textpassagen.
// In Microsoft Word können wir die Form anklicken und zu einem beliebigen Absatz ziehen, als wäre es ein Zeichen.
// Wenn die Form groß ist, wirkt sich dies auf den vertikalen Absatzabstand aus.
// Wir können diese Form nicht an eine Stelle ohne Absatz verschieben.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Floating:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Eine schwebende Form gehört zu dem Absatz, in den wir sie einfügen,
// was wir durch ein Ankersymbol feststellen können, das erscheint, wenn wir auf die Form klicken.
// Wenn die Form links kein sichtbares Ankersymbol hat,
// Wir müssen sichtbare Anker über "Optionen" aktivieren -> "Anzeigen" -> "Objektanker".
// In Microsoft Word können wir mit der linken Maustaste klicken und diese Form frei an eine beliebige Stelle ziehen.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


