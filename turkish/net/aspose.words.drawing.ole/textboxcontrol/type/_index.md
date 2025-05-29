---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: .NET için Aspose.Words
description: Forms 2.0 için TextBoxControl Type özelliğini keşfedin; uygulamalarınızda kusursuz denetim özelleştirmesi yapın ve kullanıcı deneyimini geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Forms 2.0 denetiminin türünü alır.

```csharp
public override Forms2OleControlType Type { get; }
```

## Örnekler

TextBox OLE denetiminin metninin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Ayrıca bakınız

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
