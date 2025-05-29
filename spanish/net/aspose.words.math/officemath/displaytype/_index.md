---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words para .NET
description: Descubra la propiedad DisplayType de OfficeMath para un formato de ecuaciones flexible: elija entre visualización en línea o independiente para una mayor claridad del documento.
type: docs
weight: 10
url: /es/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Obtiene/establece el tipo de formato de visualización de Office Math que representa si una ecuación se muestra en línea con el texto o se muestra en su propia línea.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Observaciones

El tipo de formato de visualización solo tiene efecto para Office Math de nivel superior.

El tipo de formato de visualización devuelto es siempreInline para Office Math anidado.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../../aspose.words.math/)
* asamblea [Aspose.Words](../../../)
