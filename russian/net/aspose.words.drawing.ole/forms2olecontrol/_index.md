---
title: Class Forms2OleControl
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Drawing.Ole.Forms2OleControl сорт. Представляет элемент управления OLE Microsoft Forms 2.0.
type: docs
weight: 1110
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

Представляет элемент управления OLE Microsoft Forms 2.0.

Чтобы узнать больше, посетите[Работа с объектами Ole](https://docs.aspose.com/words/net/working-with-ole-objects/) статья документации.

```csharp
public abstract class Forms2OleControl : OleControl
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | Получает свойство Caption элемента управления. Значение по умолчанию — пустая строка. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | Получает коллекцию непосредственных дочерних элементов управления. |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | Возвращает`истинный` если управление находится во включенном состоянии. |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | Получает или задает строку, задающую группу взаимоисключающих элементов управления. Значение по умолчанию — пустая строка. |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Возвращает`истинный` если контроль представляет собой`Forms2OleControl` . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Получает или задает имя элемента управления ActiveX. |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | Получает тип элемента управления Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченная кнопка выбора имеет значение «1», а неотмеченная — «0». Значение по умолчанию — пустая строка. |

### Примеры

Показывает, как проверить свойства элемента управления ActiveX.

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
    Assert.AreEqual(string.Empty, checkBox.GroupName);

    // Обратите внимание, что вы не можете установить GroupName для кадра.
    checkBox.GroupName = "Aspose group name";
}
```

### Смотрите также

* class [OleControl](../olecontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)


