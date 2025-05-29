---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.OptionButtonControl, который идеально подходит для создания эксклюзивных вариантов выбора в ваших приложениях. Улучшите пользовательский опыт сегодня!
type: docs
weight: 1510
url: /ru/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

Элемент управления OptionButton позволяет сделать один выбор из ограниченного набора взаимоисключающих вариантов.

```csharp
public class OptionButtonControl : MorphDataControl
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Получает или задает цвет фона элемента управления. Значение по умолчанию зависит от типа элемента управления. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Возвращает или задает свойство Caption элемента управления. Значение по умолчанию — пустая строка. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Получает коллекцию непосредственных дочерних элементов управления. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Возврат`истинный` если элемент управления находится во включенном состоянии. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Возвращает или задает цвет переднего плана элемента управления. Значение по умолчанию зависит от типа элемента управления. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Возвращает или задает строку, которая определяет группу взаимоисключающих элементов управления. Значением по умолчанию является пустая строка. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Возвращает или задает высоту элемента управления в пунктах. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Возврат`истинный` если контроль - это[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Возвращает или задает имя элемента управления ActiveX. |
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | Возвращает или задает логическое значение, указывающее, что это`OptionButtonControl` выбран или нет. |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | Получает тип элемента управления Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченный переключатель имеет значение «1», а неотмеченный — «0». Значение по умолчанию — пустая строка. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Возвращает или задает ширину элемента управления в пунктах. |

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

* class [MorphDataControl](../morphdatacontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
