---
title: OfficeMath.ParentParagraph
linktitle: ParentParagraph
articleTitle: ParentParagraph
second_title: Aspose.Words per .NET
description: OfficeMath ParentParagraph proprietà. Recupera il genitoreParagraph di questo nodo in C#.
type: docs
weight: 50
url: /it/net/aspose.words.math/officemath/parentparagraph/
---
## OfficeMath.ParentParagraph property

Recupera il genitore[`Paragraph`](../../../aspose.words/paragraph/) di questo nodo.

```csharp
public Paragraph ParentParagraph { get; }
```

## Esempi

Mostra come impostare la formattazione della visualizzazione della matematica di Office.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath) doc.GetChild(NodeType.OfficeMath, 0, true);

// I nodi OfficeMath che sono figli di altri nodi OfficeMath sono sempre in linea.
// Il nodo con cui stiamo lavorando è il nodo base per modificarne la posizione e il tipo di visualizzazione.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Modifica la posizione e il tipo di visualizzazione del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Guarda anche

* class [Paragraph](../../../aspose.words/paragraph/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../../aspose.words.math/)
* assemblea [Aspose.Words](../../../)
