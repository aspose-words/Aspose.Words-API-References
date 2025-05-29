---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.CheckBoxControl, который позволяет легко переключать значения флажков и расширять возможности автоматизации документов за счет бесшовной интеграции.
type: docs
weight: 1440
url: /ru/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

Элемент управления CheckBox переключает значение.

```csharp
public class CheckBoxControl : MorphDataControl
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | Получает или задает цвет фона элемента управления. Значение по умолчанию зависит от типа элемента управления. |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | Возвращает или задает свойство Caption элемента управления. Значение по умолчанию — пустая строка. |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | Возвращает или задает логическое значение, указывающее, что это`CheckBoxControl` проверено или нет. Значение по умолчанию:`ЛОЖЬ` . |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Получает коллекцию непосредственных дочерних элементов управления. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Возврат`истинный` если элемент управления находится во включенном состоянии. |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | Возвращает или задает цвет переднего плана элемента управления. Значение по умолчанию зависит от типа элемента управления. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Возвращает или задает строку, которая определяет группу взаимоисключающих элементов управления. Значением по умолчанию является пустая строка. |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | Возвращает или задает высоту элемента управления в пунктах. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Возврат`истинный` если контроль - это[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Возвращает или задает имя элемента управления ActiveX. |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | Получает тип элемента управления Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченный переключатель имеет значение «1», а неотмеченный — «0». Значение по умолчанию — пустая строка. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Возвращает или задает ширину элемента управления в пунктах. |

## Примечания

Он имеет три возможных состояния: выбрано, очищено и не выбрано и не очищено, что означает комбинацию включенного и выключенного состояний.

## Примеры

Показывает, как изменить состояние элемента управления CheckBox.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### Смотрите также

* class [MorphDataControl](../morphdatacontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
