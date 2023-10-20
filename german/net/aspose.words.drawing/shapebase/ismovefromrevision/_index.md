---
title: ShapeBase.IsMoveFromRevision
linktitle: IsMoveFromRevision
articleTitle: IsMoveFromRevision
second_title: Aspose.Words für .NET
description: ShapeBase IsMoveFromRevision eigendom. Gibt zurückWAHR wenn dieses Objekt in Microsoft Word verschoben gelöscht wurde während die Änderungsverfolgung aktiviert war in C#.
type: docs
weight: 320
url: /de/net/aspose.words.drawing/shapebase/ismovefromrevision/
---
## ShapeBase.IsMoveFromRevision property

Gibt zurück`WAHR` wenn dieses Objekt in Microsoft Word verschoben (gelöscht) wurde, während die Änderungsverfolgung aktiviert war.

```csharp
public bool IsMoveFromRevision { get; }
```

## Beispiele

Zeigt, wie Verschiebungsrevisionsformen identifiziert werden.

```csharp
// Eine Verschiebungsrevision liegt vor, wenn wir ein Element im Dokumentkörper verschieben, indem wir es in Microsoft Word ausschneiden und einfügen
// Änderungen verfolgen. Wenn wir eine Inline-Form in eine solche Textbewegung einbeziehen, ist diese Form ebenfalls eine Revision.
// Beim Kopieren und Einfügen oder Verschieben schwebender Formen werden keine Verschiebungsrevisionen erstellt.
Document doc = new Document(MyDir + "Revision shape.docx");

// Verschieberevisionen bestehen aus Paaren von „Verschieben von“- und „Verschieben nach“-Revisionen. Wir haben dieses Dokument in einer Form verschoben,
// aber bis wir die Verschiebungsrevision akzeptieren oder ablehnen, wird es zwei Instanzen dieser Form geben.
Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(2, shapes.Length);

// Dies ist die „Move to“-Revision, also die Form am Zielort.
// Wenn wir die Revision akzeptieren, verschwindet diese „Verschieben nach“-Revisionsform.
// und die Revisionsform „Verschieben von“ bleibt erhalten.
Assert.False(shapes[0].IsMoveFromRevision);
Assert.True(shapes[0].IsMoveToRevision);

// Dies ist die „Move from“-Revision, also die Form an ihrem ursprünglichen Standort.
// Wenn wir die Revision akzeptieren, verschwindet diese „Verschieben von“-Revisionsform.
// und die Revisionsform „Verschieben nach“ bleibt erhalten.
Assert.True(shapes[1].IsMoveFromRevision);
Assert.False(shapes[1].IsMoveToRevision);
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
