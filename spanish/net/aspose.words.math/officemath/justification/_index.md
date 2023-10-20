---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words para .NET
description: OfficeMath Justification propiedad. Obtiene/establece la justificación de Office Math en C#.
type: docs
weight: 20
url: /es/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Obtiene/establece la justificación de Office Math.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Observaciones

La justificación no se puede establecer en Office Math con el tipo de formato de visualizaciónInline.

La justificación en línea no se puede configurar en Office Math con el tipo de formato de visualizaciónDisplay.

Correspondiente[`DisplayType`](../displaytype/) debe configurarse antes de configurar la justificación de Office Math.

## Ejemplos

Muestra cómo configurar el formato de visualización de matemáticas de Office.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Los nodos de OfficeMath que son hijos de otros nodos de OfficeMath siempre están en línea.
// El nodo con el que estamos trabajando es el nodo base para cambiar su ubicación y tipo de visualización.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Cambiar la ubicación y el tipo de visualización del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ver también

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../../aspose.words.math/)
* asamblea [Aspose.Words](../../../)
