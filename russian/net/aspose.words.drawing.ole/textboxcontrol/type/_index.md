---
title: TextBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство TextBoxControl Type для Forms 2.0, обеспечивающее беспрепятственную настройку элементов управления и улучшающее взаимодействие с пользователем в ваших приложениях.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.ole/textboxcontrol/type/
---
## TextBoxControl.Type property

Получает тип элемента управления Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [TextBoxControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
