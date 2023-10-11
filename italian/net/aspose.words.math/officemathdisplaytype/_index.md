---
title: Enum OfficeMathDisplayType
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Math.OfficeMathDisplayType enum. Specifica il tipo di formato di visualizzazione dellequazione.
type: docs
weight: 4130
url: /it/net/aspose.words.math/officemathdisplaytype/
---
## OfficeMathDisplayType enumeration

Specifica il tipo di formato di visualizzazione dell'equazione.

```csharp
public enum OfficeMathDisplayType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Display | `0` | Office Math viene visualizzato su una riga separata. |
| Inline | `1` | Office Math viene visualizzato in linea con il testo. |

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

* spazio dei nomi [Aspose.Words.Math](../../aspose.words.math/)
* assemblea [Aspose.Words](../../)


