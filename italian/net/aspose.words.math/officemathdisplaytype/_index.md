---
title: OfficeMathDisplayType Enum
linktitle: OfficeMathDisplayType
articleTitle: OfficeMathDisplayType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.Math.OfficeMathDisplayType per personalizzare facilmente i formati di visualizzazione delle equazioni, migliorando la chiarezza e la presentazione dei documenti.
type: docs
weight: 4820
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

* spazio dei nomi [Aspose.Words.Math](../../aspose.words.math/)
* assemblea [Aspose.Words](../../)
