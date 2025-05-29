---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words für .NET
description: Steuern Sie die Sichtbarkeit von Formen mit der versteckten Eigenschaft von ShapeBase. Wechseln Sie einfach zwischen sichtbar und versteckt für mehr Designflexibilität.
type: docs
weight: 230
url: /de/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob die Form sichtbar ist.

```csharp
public bool Hidden { get; set; }
```

## Bemerkungen

Der Standardwert ist`FALSCH` .

## Beispiele

Zeigt, wie die Form ausgeblendet wird.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
