---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Math.OfficeMathDisplayType para personalizar fácilmente los formatos de visualización de ecuaciones para mejorar la claridad y presentación del documento.
type: docs
weight: 4820
url: /es/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Especifica el tipo de formato de visualización de la ecuación.

```csharp
public enum OfficeMathDisplayType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Display | `0` | La función Office Math se muestra en su propia línea. |
| Inline | `1` | La función Office Math se muestra en línea con el texto. |

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

* espacio de nombres [Aspose.Words.Math](../../aspose.words.math/)
* asamblea [Aspose.Words](../../)
