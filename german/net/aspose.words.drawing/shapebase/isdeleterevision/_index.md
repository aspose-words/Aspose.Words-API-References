---
title: ShapeBase.IsDeleteRevision
linktitle: IsDeleteRevision
articleTitle: IsDeleteRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „IsDeleteRevision“ und erfahren Sie, wie sie das Löschen von Objekten in Microsoft Word mit aktivierter Änderungsverfolgung für eine verbesserte Dokumentverwaltung anzeigt.
type: docs
weight: 270
url: /de/net/aspose.words.drawing/shapebase/isdeleterevision/
---
## ShapeBase.IsDeleteRevision property

Gibt „true“ zurück, wenn dieses Objekt in Microsoft Word gelöscht wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsDeleteRevision { get; }
```

## Beispiele

Zeigt, wie mit Revisionsformen gearbeitet wird.

```csharp
Document doc = new Document();

Assert.False(doc.TrackRevisions);

// Fügen Sie eine Inline-Form ein, ohne Revisionen zu verfolgen. Dadurch wird diese Form zu keiner Revision jeglicher Art.
Shape shape = new Shape(doc, ShapeType.Cube);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

// Beginnen Sie mit der Verfolgung von Revisionen und fügen Sie dann eine weitere Form ein, die eine Revision sein wird.
doc.StartTrackRevisions("John Doe");

shape = new Shape(doc, ShapeType.Sun);
shape.WrapType = WrapType.Inline;
shape.Width = 100.0;
shape.Height = 100.0;
doc.FirstSection.Body.FirstParagraph.AppendChild(shape);

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

shapes[0].Remove();

// Da wir diese Form entfernt haben, während wir die Änderungen verfolgt haben,
// Die Form bleibt im Dokument bestehen und zählt als gelöschte Revision.
// Wenn Sie diese Überarbeitung akzeptieren, wird die Form dauerhaft entfernt, und wenn Sie sie ablehnen, bleibt sie im Dokument.
Assert.AreEqual(ShapeType.Cube, shapes[0].ShapeType);
Assert.True(shapes[0].IsDeleteRevision);

// Und wir haben beim Nachverfolgen der Änderungen eine weitere Form eingefügt, sodass diese Form als eingefügte Revision zählt.
// Durch die Annahme dieser Revision wird diese Form als Nicht-Revision in das Dokument aufgenommen.
// und das Ablehnen der Revision wird diese Form dauerhaft entfernen.
Assert.AreEqual(ShapeType.Sun, shapes[1].ShapeType);
Assert.True(shapes[1].IsInsertRevision);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
