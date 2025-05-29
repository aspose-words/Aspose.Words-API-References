---
title: CommandButtonControl Class
linktitle: CommandButtonControl
articleTitle: CommandButtonControl
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.CommandButtonControl, чтобы легко создавать интерактивные кнопки, запускающие макросы, повышая вовлеченность пользователей в ваши приложения.
type: docs
weight: 1450
url: /ru/net/aspose.words.drawing.ole/commandbuttoncontrol/
---
## CommandButtonControl class

Элемент управления CommandButton запускает макрос, который выполняет действие, когда пользователь нажимает на него.

```csharp
public class CommandButtonControl : Forms2OleControl
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [CommandButtonControl](commandbuttoncontrol/)() | Инициализирует новый экземпляр`CommandButtonControl` класс. |

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
| override [Type](../../aspose.words.drawing.ole/commandbuttoncontrol/type/) { get; } | Получает тип элемента управления Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченный переключатель имеет значение «1», а неотмеченный — «0». Значение по умолчанию — пустая строка. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Возвращает или задает ширину элемента управления в пунктах. |

## Примеры

Показывает, как вставить элемент управления ActiveX.

```csharp
DocumentBuilder builder = new DocumentBuilder();

CommandButtonControl button1 = new CommandButtonControl();
Shape shape = builder.InsertForms2OleControl(button1);
Assert.AreEqual(Forms2OleControlType.CommandButton, button1.Type);
```

### Смотрите также

* class [Forms2OleControl](../forms2olecontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
