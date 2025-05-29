---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words för .NET
description: Upptäck egenskapen TextBoxControl Type för Forms 2.0, som möjliggör sömlös kontrollanpassning och förbättrar användarupplevelsen i dina applikationer.
type: docs
weight: 20
url: /sv/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Hämtar typ av Forms 2.0-kontroll.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* namnutrymme [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* hopsättning [Aspose.Words](../../../)
