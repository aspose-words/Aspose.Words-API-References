---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words per .NET
description: Scopri la proprietà OptionButtonControl Type per Forms 2.0. Scopri come migliorare i tuoi form con questa funzionalità essenziale per i tipi di controllo.
type: docs
weight: 20
url: /it/net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

Ottiene il tipo di controllo Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## Esempi

Mostra come selezionare il pulsante di scelta.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Deseleziona il primo elemento selezionato.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Seleziona il secondo pulsante di opzione.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Guarda anche

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* spazio dei nomi [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* assemblea [Aspose.Words](../../../)
