---
title: ShapeBase.IsInline
linktitle: IsInline
articleTitle: IsInline
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „IsInline“, um einfach zu überprüfen, ob Ihre Form mit dem Text übereinstimmt, wodurch Ihr Design verbessert und die Layouteffizienz gesteigert wird.
type: docs
weight: 310
url: /de/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Eine schnelle Möglichkeit, festzustellen, ob diese Form inline mit Text positioniert ist.

```csharp
public bool IsInline { get; }
```

## Bemerkungen

Wirkt sich nur auf Formen der obersten Ebene aus.

## Beispiele

Zeigt, wie ermittelt wird, ob eine Form eingebettet oder schwebend ist.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Unten sind zwei Umbrucharten aufgeführt, die Formen haben können.
// 1 - Inline:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Eine Inline-Form befindet sich innerhalb eines Absatzes zwischen anderen Absatzelementen, beispielsweise Textläufen.
// In Microsoft Word können wir die Form anklicken und in einen beliebigen Absatz ziehen, als wäre sie ein Zeichen.
// Wenn die Form groß ist, wirkt sich dies auf den vertikalen Absatzabstand aus.
// Wir können diese Form nicht an eine Stelle ohne Absatz verschieben.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Schwebend:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 200,
    RelativeVerticalPosition.TopMargin, 200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Eine schwebende Form gehört zu dem Absatz, in den wir sie einfügen,
// was wir anhand eines Ankersymbols erkennen können, das erscheint, wenn wir auf die Form klicken.
// Wenn die Form links kein sichtbares Ankersymbol hat,
// Wir müssen sichtbare Anker über „Optionen“ -> „Anzeige“ -> „Objektanker“ aktivieren.
// In Microsoft Word können wir mit der linken Maustaste klicken und diese Form frei an eine beliebige Stelle ziehen.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
