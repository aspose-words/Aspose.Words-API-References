---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „ShadowFormat Visible“. Überprüfen Sie ganz einfach, ob Ihre Formatierung sichtbar ist, und verbessern Sie so das Erscheinungsbild und die Übersichtlichkeit Ihres Dokuments.
type: docs
weight: 30
url: /de/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Rückgaben`WAHR` wenn die auf diese Instanz angewendete Formatierung sichtbar ist.

```csharp
public bool Visible { get; }
```

## Bemerkungen

Im Gegensatz[`Clear`](../clear/) , Zuweisen`FALSCH`auf Sichtbar löscht die Formatierung nicht, es blendet nur den Formeffekt aus.

## Beispiele

Zeigt, wie mit einer Schattenformatierung für die Form gearbeitet wird.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### Siehe auch

* class [ShadowFormat](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
