---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words für .NET
description: ShapeBase IsTopLevel eigendom. Gibt zurückWAHRwenn diese Form kein untergeordnetes Element einer Gruppenform ist in C#.
type: docs
weight: 350
url: /de/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Gibt zurück`WAHR`wenn diese Form kein untergeordnetes Element einer Gruppenform ist.

```csharp
public bool IsTopLevel { get; }
```

## Beispiele

Zeigt, wie man erkennt, ob eine Form Teil einer Gruppenform ist.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Eine Form ist standardmäßig nicht Teil einer Gruppenform und daher ist die Eigenschaft „IsTopLevel“ auf „true“ gesetzt.
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Sobald wir eine Form in eine Gruppenform assimilieren, ändert sich die Eigenschaft „IsTopLevel“ in „false“.
Assert.False(shape.IsTopLevel);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
