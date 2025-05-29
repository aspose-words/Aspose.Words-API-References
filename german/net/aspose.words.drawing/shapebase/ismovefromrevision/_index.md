---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „IsMoveFromRevision“ in Microsoft Word. Verfolgen Sie Änderungen ganz einfach und identifizieren Sie verschobene oder gelöschte Objekte präzise.
type: docs
weight: 340
url: /de/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Rückgaben`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveFromRevision { get; }
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
