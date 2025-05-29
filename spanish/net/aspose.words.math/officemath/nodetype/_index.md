---
title: OfficeMath.NodeType
linktitle: NodeType
articleTitle: NodeType
second_title: Aspose.Words para .NET
description: Descubra la propiedad OfficeMath NodeType que devuelve de manera eficiente elementos OfficeMath, mejorando las capacidades matemáticas de su documento.
type: docs
weight: 40
url: /es/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

DevuelveOfficeMath .

```csharp
public override NodeType NodeType { get; }
```

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

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* espacio de nombres [Aspose.Words.Math](../../../aspose.words.math/)
* asamblea [Aspose.Words](../../../)
