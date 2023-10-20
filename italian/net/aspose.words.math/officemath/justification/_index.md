---
title: OfficeMath.Justification
linktitle: Justification
articleTitle: Justification
second_title: Aspose.Words per .NET
description: OfficeMath Justification proprietà. Ottiene/imposta la giustificazione matematica di Office in C#.
type: docs
weight: 20
url: /it/net/aspose.words.math/officemath/justification/
---
## OfficeMath.Justification property

Ottiene/imposta la giustificazione matematica di Office.

```csharp
public OfficeMathJustification Justification { get; set; }
```

## Osservazioni

La giustificazione non può essere impostata su Office Math con il tipo di formato di visualizzazioneInline.

La giustificazione in linea non può essere impostata sul tipo Office Math con formato di visualizzazioneDisplay.

Corrispondente[`DisplayType`](../displaytype/) deve essere impostato prima di impostare la giustificazione matematica di Office.

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

* enum [OfficeMathJustification](../../officemathjustification/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../../aspose.words.math/)
* assemblea [Aspose.Words](../../../)
