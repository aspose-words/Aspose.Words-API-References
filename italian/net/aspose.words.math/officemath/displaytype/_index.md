---
title: OfficeMath.DisplayType
second_title: Aspose.Words per .NET API Reference
description: OfficeMath proprietà. Ottiene/imposta il tipo di formato di visualizzazione di Office Math che rappresenta se unequazione viene visualizzata in linea con il testo o visualizzata su una riga separata.
type: docs
weight: 10
url: /it/net/aspose.words.math/officemath/displaytype/
---
## OfficeMath.DisplayType property

Ottiene/imposta il tipo di formato di visualizzazione di Office Math che rappresenta se un'equazione viene visualizzata in linea con il testo o visualizzata su una riga separata.

```csharp
public OfficeMathDisplayType DisplayType { get; set; }
```

### Osservazioni

Il tipo di formato di visualizzazione ha effetto solo per Office Math di livello superiore.

Il tipo di formato di visualizzazione restituito è sempreInline per Office Math annidato.

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

* enum [OfficeMathDisplayType](../../officemathdisplaytype/)
* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../officemath/)
* assemblea [Aspose.Words](../../../)


