---
title: OfficeMath.EquationXmlEncoding
second_title: Referencia de API de Aspose.Words para .NET
description: OfficeMath propiedad. Obtiene/establece una codificación que se usó para codificar la ecuación XML si este objeto matemático de Office se lee desde ecuación XML. Usamos la codificación al guardar un documento para escribir en la misma codificación que se leyó.
type: docs
weight: 20
url: /es/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Obtiene/establece una codificación que se usó para codificar la ecuación XML, si este objeto matemático de Office se lee desde ecuación XML. Usamos la codificación al guardar un documento para escribir en la misma codificación que se leyó.

```csharp
public Encoding EquationXmlEncoding { get; set; }
```

### Ejemplos

Muestra cómo configurar el formato de visualización de Office Math.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// Los nodos de OfficeMath que son hijos de otros nodos de OfficeMath siempre están en línea.
// El nodo con el que estamos trabajando es el nodo base para cambiar su ubicación y tipo de visualización.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Los formatos OOXML y WML utilizan la propiedad "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Cambiar la ubicación y el tipo de visualización del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Ver también

* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../officemath/)
* asamblea [Aspose.Words](../../../)


