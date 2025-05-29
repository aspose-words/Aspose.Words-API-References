---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase AnchorLocked-Eigenschaft, um die Ankersperre für Formen zu steuern und so die Designstabilität und Flexibilität Ihrer Projekte zu verbessern.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Gibt an, ob der Anker der Form gesperrt ist.

```csharp
public bool AnchorLocked { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH`.

Wirkt sich nur auf Formen der obersten Ebene aus.

Diese Eigenschaft beeinflusst das Verhalten des Ankers der Form in Microsoft Word. Wenn der Anker nicht gesperrt ist, kann beim Verschieben der Form in Microsoft Word auch der Anker der Form verschoben werden.

## Beispiele

Zeigt, wie Sie den Absatzanker einer Form sperren oder entsperren.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Setzen Sie die Eigenschaft "AnchorLocked" auf "true", um zu verhindern, dass der Anker der Form
// vor dem Verschieben beim Verschieben der Form in Microsoft Word.
// Setzen Sie die Eigenschaft "AnchorLocked" auf "false", um jede Bewegung der Form zuzulassen
// um seinen Anker auch in jeden anderen Absatz zu verschieben, in dessen Nähe sich die Form befindet.
shape.AnchorLocked = anchorLocked;

// Wenn die Form links kein sichtbares Ankersymbol hat,
// Wir müssen sichtbare Anker über „Optionen“ -> „Anzeige“ -> „Objektanker“ aktivieren.
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
