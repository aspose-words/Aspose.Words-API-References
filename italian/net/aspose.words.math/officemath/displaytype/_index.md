---
title: OfficeMath.DisplayType
second_title: Aspose.Words per .NET API Reference
description: OfficeMath proprietà. Ottiene/imposta il tipo di formato di visualizzazione Office Math che indica se unequazione viene visualizzata in linea con il testo o su una propria riga.
type: docs
weight: 10
url: /it/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Ottiene/imposta il tipo di formato di visualizzazione Office Math che indica se un'equazione viene visualizzata in linea con il testo o su una propria riga.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Osservazioni

Il tipo di formato di visualizzazione ha effetto solo per Office Math di livello superiore.

Il tipo di formato di visualizzazione restituito è sempreInline per Office Math nidificato.

### Esempi

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../officemath/)
* assemblea [Aspose.Words](../../../)


