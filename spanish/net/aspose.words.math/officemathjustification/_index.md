---
title: OfficeMathJustification Enum
linktitle: OfficeMathJustification
articleTitle: OfficeMathJustification
second_title: Aspose.Words para .NET
description: Aspose.Words.Math.OfficeMathJustification enumeración. Especifica la justificación de la ecuación en C#.
type: docs
weight: 4140
url: /es/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Especifica la justificación de la ecuación.

```csharp
public enum OfficeMathJustification
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| CenterGroup | `1` | Justifica instancias de texto matemático a la izquierda entre sí y centra el grupo de texto math (el párrafo matemático) con respecto a la página. |
| Center | `2` | Centra cada instancia de texto matemático individualmente con respecto a los márgenes. |
| Left | `3` | Justificación izquierda del párrafo matemático. |
| Right | `4` | Justificación correcta del párrafo matemático. |
| Inline | `7` | Posición en línea de Math. |
| Default | `1` | Valor predeterminadoCenterGroup . |

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

* espacio de nombres [Aspose.Words.Math](../../aspose.words.math/)
* asamblea [Aspose.Words](../../)
