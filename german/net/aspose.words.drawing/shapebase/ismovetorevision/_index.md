---
title: ShapeBase.IsMoveToRevision
linktitle: IsMoveToRevision
articleTitle: IsMoveToRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die IsMoveToRevision-Eigenschaft von ShapeBase Ihr Microsoft Word-Erlebnis verbessert, indem sie Objektbewegungen während der Bearbeitung nahtlos verfolgt.
type: docs
weight: 350
url: /de/net/aspose.words.drawing/shapebase/ismovetorevision/
---
## ShapeBase.IsMoveToRevision property

Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (eingefügt) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveToRevision { get; }
```

## Beispiele

Zeigt, wie verschobene Revisionsformen identifiziert werden.

```csharp
// Eine Verschiebungsrevision liegt vor, wenn wir ein Element im Dokumentkörper verschieben, indem wir es in Microsoft Word ausschneiden und einfügen, während
// Änderungen verfolgen. Wenn wir eine Inline-Form in eine solche Textbewegung einbeziehen, wird diese Form auch eine Überarbeitung sein.
// Durch Kopieren und Einfügen oder Verschieben schwebender Formen werden keine Verschiebungsrevisionen erstellt.
Document doc = new Document(MyDir + "Revision shape.docx");

// Verschieberevisionen bestehen aus Paaren von "Verschieben von" und "Verschieben nach". Wir haben dieses Dokument in einer Form verschoben,
// aber bis wir die Verschiebungsrevision akzeptieren oder ablehnen, wird es zwei Instanzen dieser Form geben.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Dies ist die „Verschieben nach“-Revision, also die Form an ihrem Zielort.
// Wenn wir die Revision akzeptieren, verschwindet diese Revisionsform „Verschieben nach“.
// und die Revisionsform „Verschieben von“ bleibt erhalten.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Dies ist die „Verschieben von“-Revision, also die Form an ihrem ursprünglichen Speicherort.
// Wenn wir die Revision akzeptieren, verschwindet diese Revisionsform „Verschieben von“,
// und die Revisionsform „Verschieben nach“ bleibt erhalten.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
