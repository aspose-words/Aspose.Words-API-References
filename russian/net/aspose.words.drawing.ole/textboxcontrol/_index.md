---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.TextBoxControl для легкого отображения организованного текста из данных или пользовательского ввода. Улучшите управление документами сегодня!
type: docs
weight: 1520
url: /ru/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

Элемент управления TextBox отображает текст из организованного набора данных или пользовательского ввода.

```csharp
public class TextBoxControl : MorphDataControl
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
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | Получает или задает текст элемента управления. |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | Получает тип элемента управления Forms 2.0. |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | Получает базовое свойство Value, которое часто представляет состояние элемента управления. Например, отмеченный переключатель имеет значение «1», а неотмеченный — «0». Значение по умолчанию — пустая строка. |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | Возвращает или задает ширину элемента управления в пунктах. |

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

* class [MorphDataControl](../morphdatacontrol/)
* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
