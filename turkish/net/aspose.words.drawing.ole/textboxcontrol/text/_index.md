---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: .NET için Aspose.Words
description: TextBoxControl'ün metnini kolayca yönetin; uygulamanızda sorunsuz kullanıcı etkileşimi ve gelişmiş işlevsellik için içeriğini alın veya ayarlayın.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Denetimin metnini alır veya ayarlar.

```csharp
public string Text { get; set; }
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

* class [TextBoxControl](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
