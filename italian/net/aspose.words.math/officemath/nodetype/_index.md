---
title: OfficeMath.NodeType
second_title: Aspose.Words per .NET API Reference
description: OfficeMath proprietà. Restituisce NodeType.OfficeMath .
type: docs
weight: 50
url: /it/net/aspose.words.math/officemath/nodetype/
---
## OfficeMath.NodeType property

Restituisce **NodeType.OfficeMath** .

```csharp
public override NodeType NodeType { get; }
```

### Esempi

Mostra come impostare la formattazione della visualizzazione matematica dell'ufficio.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// I nodi OfficeMath che sono figli di altri nodi OfficeMath sono sempre inline.
// Il nodo con cui stiamo lavorando è il nodo base per cambiarne la posizione e il tipo di visualizzazione.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// I formati OOXML e WML utilizzano la proprietà "EquationXmlEncoding".
Assert.IsNull(officeMath.EquationXmlEncoding);

// Modifica la posizione e il tipo di visualizzazione del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Guarda anche

* enum [NodeType](../../../aspose.words/nodetype/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../officemath/)
* assemblea [Aspose.Words](../../../)


