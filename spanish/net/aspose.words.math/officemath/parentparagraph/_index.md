---
title: OfficeMath.ParentParagraph
second_title: Referencia de API de Aspose.Words para .NET
description: OfficeMath propiedad. Recupera el padreParagraph de este nodo.
type: docs
weight: 50
url: /es/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Recupera el padre[`Paragraph`](../../../aspose.words/paragraph/) de este nodo.

```csharp
public Paragraph ParentParagraph { get; }
```

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

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../officemath/)
* asamblea [Aspose.Words](../../../)


