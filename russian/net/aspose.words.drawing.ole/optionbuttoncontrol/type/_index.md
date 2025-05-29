---
title: OptionButtonControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words для .NET
description: Откройте для себя свойство OptionButtonControl Type для Forms 2.0. Узнайте, как улучшить ваши формы с помощью этой важной функции типа элемента управления.
type: docs
weight: 20
url: /ru/net/aspose.words.drawing.ole/optionbuttoncontrol/type/
---
## OptionButtonControl.Type property

Получает тип элемента управления Forms 2.0.

```csharp
public override Forms2OleControlType Type { get; }
```

## Примеры

Показывает, как выбрать переключатель.

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// Отменить выбор первого выбранного элемента.
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// Выберите вторую кнопку выбора.
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### Смотрите также

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [OptionButtonControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
