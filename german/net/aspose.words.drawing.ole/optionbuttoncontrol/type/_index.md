---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die OptionButtonControl Type-Eigenschaft für Forms 2.0. Erfahren Sie, wie Sie Ihre Formulare mit dieser wichtigen Steuerelementfunktion verbessern können.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

Ruft den Typ des Forms 2.0-Steuerelements ab.

```csharp
public override Forms2OleControlType Type { get; }
```

## Beispiele

Zeigt, wie ein Optionsfeld ausgewählt wird.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Auswahl des ersten ausgewählten Elements aufheben.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Wählen Sie die zweite Optionsschaltfläche aus.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Siehe auch

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
