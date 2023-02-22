---
title: ShapeBase.IsTopLevel
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Gibt wahr zurück wenn diese Form kein untergeordnetes Element einer Gruppenform ist.
type: docs
weight: 340
url: /de/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Gibt wahr zurück, wenn diese Form kein untergeordnetes Element einer Gruppenform ist.

```csharp
public bool IsTopLevel { get; }
```

### Beispiele

Zeigt, wie Sie feststellen können, ob ein Shape Teil eines Gruppen-Shapes ist.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Eine Form ist standardmäßig nicht Teil einer Gruppenform und hat daher die Eigenschaft "IsTopLevel" auf "true".
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Sobald wir eine Form in eine Gruppenform assimilieren, ändert sich die Eigenschaft "IsTopLevel" in "false".
Assert.False(shape.IsTopLevel);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


