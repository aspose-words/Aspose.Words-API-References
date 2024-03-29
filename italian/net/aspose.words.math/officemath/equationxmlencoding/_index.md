---
title: OfficeMath.EquationXmlEncoding
second_title: Aspose.Words per .NET API Reference
description: OfficeMath proprietà. Ottiene/imposta una codifica utilizzata per codificare lXML dellequazione se questo oggetto matematico dellufficio viene letto dallXML dellequazione . Usiamo la codifica sul salvataggio di un documento per scrivere nella stessa codifica in cui è stato letto.
type: docs
weight: 20
url: /it/net/aspose.words.math/officemath/equationxmlencoding/
---
## OfficeMath.EquationXmlEncoding property

Ottiene/imposta una codifica utilizzata per codificare l'XML dell'equazione, se questo oggetto matematico dell'ufficio viene letto dall'XML dell'equazione . Usiamo la codifica sul salvataggio di un documento per scrivere nella stessa codifica in cui è stato letto.

```csharp
public Encoding EquationXmlEncoding { get; set; }
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

* class [OfficeMath](../)
* spazio dei nomi [Aspose.Words.Math](../../officemath/)
* assemblea [Aspose.Words](../../../)


