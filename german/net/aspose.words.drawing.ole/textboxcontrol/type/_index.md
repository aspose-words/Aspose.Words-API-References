---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „TextBoxControl Type“ für Forms 2.0, die eine nahtlose Steuerelementanpassung ermöglicht und das Benutzererlebnis in Ihren Anwendungen verbessert.
type: docs
weight: 20
url: /de/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Ruft den Typ des Forms 2.0-Steuerelements ab.

```csharp
public override Forms2OleControlType Type { get; }
```

## Beispiele

Zeigt, wie der Text des TextBox-OLE-Steuerelements geändert wird.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Siehe auch

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
