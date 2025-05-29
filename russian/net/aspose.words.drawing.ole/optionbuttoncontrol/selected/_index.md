---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words для .NET
description: Управляйте своим OptionButtonControl с легкостью! Устанавливайте или получайте его выбранное состояние с помощью простого логического значения для бесперебойного взаимодействия с пользователем.
type: docs
weight: 10
url: /ru/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

Возвращает или задает логическое значение, указывающее, что это[`OptionButtonControl`](../) выбран или нет.

```csharp
public bool Selected { get; set; }
```

## Примечания

Обратите внимание, что это свойство позволяет вам выбрать несколько элементов в группе[`OptionButtonControl`](../) с тем же[`GroupName`](../../forms2olecontrol/groupname/) . Вам нужно позаботиться об отмене выбора ранее выбранного элемента, когда вы делаете это.[`OptionButtonControl`](../) выбрано.

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

* class [OptionButtonControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
