---
title: TextBoxControl.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words для .NET
description: Легко управляйте текстом TextBoxControl — получайте или задавайте его содержимое для бесперебойного взаимодействия с пользователем и расширения функциональных возможностей вашего приложения.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/textboxcontrol/text/
---
## TextBoxControl.Text property

Получает или задает текст элемента управления.

```csharp
public string Text { get; set; }
```

## Примеры

Показывает, как изменить текст элемента управления OLE TextBox.

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### Смотрите также

* class [TextBoxControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
