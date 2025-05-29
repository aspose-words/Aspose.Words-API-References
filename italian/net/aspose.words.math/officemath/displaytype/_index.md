---
title: OfficeMath.DisplayType
linktitle: DisplayType
articleTitle: DisplayType
second_title: Aspose.Words per .NET
description: Scopri la proprietà DisplayType di OfficeMath per una formattazione flessibile delle equazioni: scegli tra visualizzazione in linea o autonoma per una maggiore chiarezza del documento.
type: docs
weight: 10
url: /it/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Ottiene/imposta il tipo di formato di visualizzazione di Office Math che indica se un'equazione viene visualizzata in linea con il testo o su una riga a parte.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

## Osservazioni

Il tipo di formato di visualizzazione ha effetto solo per Office Math di livello superiore.

Il tipo di formato di visualizzazione restituito è sempreInline per Office Math annidato.

## Esempi

Mostra come impostare la formattazione della visualizzazione di Office Math.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

OfficeMath officeMath = (OfficeMath)doc.GetChild(NodeType.OfficeMath, 0, true);

// I nodi OfficeMath che sono figli di altri nodi OfficeMath sono sempre in linea.
// Il nodo con cui stiamo lavorando è il nodo base per modificare la sua posizione e il tipo di visualizzazione.
Assert.AreEqual(MathObjectType.OMathPara, officeMath.MathObjectType);
Assert.AreEqual(NodeType.OfficeMath, officeMath.NodeType);
Assert.AreEqual(officeMath.ParentNode, officeMath.ParentParagraph);

// Modifica la posizione e il tipo di visualizzazione del nodo OfficeMath.
officeMath.DisplayType = OfficeMathDisplayType.Display;
officeMath.Justification = OfficeMathJustification.Left;

doc.Save(ArtifactsDir + "Shape.OfficeMath.docx");
```

### Guarda anche

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../../aspose.words.math/)
* assemblea [Aspose.Words](../../../)
