---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà TextBoxControl Type per Forms 2.0, che consente una personalizzazione fluida dei controlli e migliora l'esperienza utente nelle tue applicazioni.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Ottiene il tipo di controllo Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## Esempi

Mostra come modificare il testo del controllo OLE TextBox.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Guarda anche

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
