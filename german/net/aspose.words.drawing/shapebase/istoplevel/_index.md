---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: Aspose.Words für .NET
description: Entdecken Sie ShapeBase IsTopLevel. Überprüfen Sie schnell, ob eine Form allein steht, und verbessern Sie Ihren Design-Workflow durch effizientes Gruppenmanagement.
type: docs
weight: 370
url: /de/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Rückgaben`WAHR` wenn diese Form kein untergeordnetes Element einer Gruppenform ist.

```csharp
public bool IsTopLevel { get; }
```

## Beispiele

Zeigt, wie Sie erkennen, ob eine Form Teil einer Gruppenform ist.

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

// Sobald wir eine Form in eine Gruppenform integrieren, ändert sich die Eigenschaft „IsTopLevel“ in „false“.
Assert.False(shape.IsTopLevel);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
