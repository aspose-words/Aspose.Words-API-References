---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words für .NET
description: Verwalten Sie den Text des TextBoxControl ganz einfach – rufen Sie seinen Inhalt ab oder legen Sie ihn fest, um eine nahtlose Benutzerinteraktion und erweiterte Funktionalität in Ihrer Anwendung zu ermöglichen.
type: docs
weight: 10
url: /de/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Ruft einen Text des Steuerelements ab oder legt ihn fest.

```csharp
public string Text { get; set; }
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

* class [TextBoxControl](../)
* namensraum [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* Montage [Aspose.Words](../../../)
