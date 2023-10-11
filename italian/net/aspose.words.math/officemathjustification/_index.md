---
title: Enum OfficeMathJustification
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Math.OfficeMathJustification enum. Specifica la giustificazione dellequazione.
type: docs
weight: 4140
url: /it/net/aspose.words.math/officemathjustification/
---
## OfficeMathJustification enumeration

Specifica la giustificazione dell'equazione.

```csharp
public enum OfficeMathJustification
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| CenterGroup | `1` | Giustifica le istanze di testo matematico a sinistra l'una rispetto all'altra e centra il gruppo di testo matematico (il paragrafo matematico) rispetto alla pagina. |
| Center | `2` | Centra ogni istanza del testo matematico individualmente rispetto ai margini. |
| Left | `3` | Giustificazione a sinistra del paragrafo matematico. |
| Right | `4` | Giustificazione corretta del paragrafo matematico. |
| Inline | `7` | Posizione in linea di Math. |
| Default | `1` | Valore predefinitoCenterGroup . |

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


