---
title: OfficeMath.DisplayType
second_title: Referencia de API de Aspose.Words para .NET
description: OfficeMath propiedad. Obtiene/establece el tipo de formato de visualización de Office Math que representa si una ecuación se muestra en línea con el texto o se muestra en su propia línea.
type: docs
weight: 10
url: /es/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Obtiene/establece el tipo de formato de visualización de Office Math que representa si una ecuación se muestra en línea con el texto o se muestra en su propia línea.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Observaciones

El tipo de formato de visualización tiene efecto solo para Office Math de nivel superior.

El tipo de formato de visualización devuelto es siempreInline para Office Math anidado.

### Ejemplos

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../officemath/)
* asamblea [Aspose.Words](../../../)


