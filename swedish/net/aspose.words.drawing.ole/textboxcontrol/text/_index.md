---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words för .NET
description: Hantera TextBoxControls text enkelt – hämta eller ställ in dess innehåll för sömlös användarinteraktion och förbättrad funktionalitet i din applikation.
type: docs
weight: 10
url: /sv/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Hämtar eller anger en text från kontrollen.

```csharp
public string Text { get; set; }
```

## Exempel

Visar hur man ändrar texten i TextBox OLE-kontrollen.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Se även

* class [TextBoxControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
