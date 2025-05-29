---
title: Forms2OleControl Class
linktitle: Forms2OleControl
articleTitle: Forms2OleControl
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.Forms2OleControl — решение для бесшовной интеграции элементов управления Microsoft Forms 2.0 OLE в ваши приложения.
type: docs
weight: 1460
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Представляет элемент управления Microsoft Forms 2.0 OLE.

Чтобы узнать больше, посетите[Работа с Ole-объектами](https://docs.aspose.com/words/net/working-with-ole-objects/) документальная статья.

```csharp
public abstract class Forms2OleControl : OleControl
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
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Возврат`истинный` если контроль - это`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Возвращает или задает имя элемента управления ActiveX. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Получает тип элемента управления Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченный переключатель имеет значение «1», а неотмеченный — «0». Значение по умолчанию — пустая строка. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Возвращает или задает ширину элемента управления в пунктах. |

## Примеры

Показывает, как проверить свойства элемента управления ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl)oleControl;
    Assert.AreEqual("First", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Обратите внимание, что вы не можете задать GroupName для фрейма.
    checkBox.GroupName = "Aspose group name";
}
```

### Смотрите также

* class [OleControl](../olecontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
