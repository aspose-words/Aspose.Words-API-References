---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words para .NET
description: Descubra la propiedad Justificación de OfficeMath para personalizar y configurar fácilmente la alineación de Office Math. ¡Mejore la presentación de sus documentos sin esfuerzo!
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

La justificación no se puede configurar en Office Math con el tipo de formato de visualizaciónInline.

La justificación en línea no se puede configurar en Office Math con el tipo de formato de visualizaciónDisplay.

Correspondiente[`DisplayType`](../displaytype/) debe configurarse antes de configurar la justificación de Office Math.

## Ejemplos

Muestra cómo configurar el formato de visualización de matemáticas de oficina.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// Los nodos OfficeMath que son hijos de otros nodos OfficeMath siempre están en línea.
//El nodo con el que estamos trabajando es el nodo base para cambiar su ubicación y tipo de visualización.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Cambia la ubicación y el tipo de visualización del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ver también

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../../aspose.words.math/)
* asamblea [Aspose.Words](../../../)
