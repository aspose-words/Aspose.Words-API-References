---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words für .NET
description: Verwalten Sie Ihr OptionButtonControl mit Leichtigkeit! Setzen oder erhalten Sie den ausgewählten Status mit einem einfachen Booleschen Wert für eine nahtlose Benutzerinteraktion.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Ruft einen booleschen Wert ab oder setzt ihn, der entweder dies angibt[`OptionButtonControl`](../) ausgewählt ist oder nicht.

```csharp
public bool Selected { get; set; }
```

## Bemerkungen

Beachten Sie, dass Sie mit dieser Eigenschaft mehrere Elemente in einer Gruppe von[`OptionButtonControl`](../) mit dem gleichen[`GroupName`](../../forms2olecontrol/groupname/) . Es liegt an Ihnen, sich um die Abwahl eines zuvor ausgewählten Elements zu kümmern, wenn Sie dies tun[`OptionButtonControl`](../) ausgewählt.

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

* class [OptionButtonControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
