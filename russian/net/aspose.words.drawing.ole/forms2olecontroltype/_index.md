---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.Ole.Forms2OleControlType, включающее ряд типов элементов управления Forms 2.0 для улучшенной автоматизации документов.
type: docs
weight: 1480
url: /ru/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

Перечисляет типы элементов управления Forms 2.0.

```csharp
public enum Forms2OleControlType
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| OptionButton | `0` | Элемент управления радиокнопкой. |
| Label | `1` | Элемент управления, отображающий текст. |
| Textbox | `2` | Элемент управления, позволяющий пользователю вводить текст. |
| CheckBox | `3` | Элемент управления, позволяющий пользователю выбрать или отменить выбор параметра. |
| ToggleButton | `4` | Элемент управления, позволяющий пользователю переключаться между двумя состояниями. |
| SpinButton | `5` | Элемент управления, позволяющий пользователю увеличивать или уменьшать значение. |
| ComboBox | `6` | Элемент управления, позволяющий пользователю выбрать элемент из списка. |
| Frame | `7` | Элемент управления, который группирует другие элементы управления. |
| MultiPage | `8` | Элемент управления, отображающий несколько страниц контента. |
| TabStrip | `9` | Элемент управления, позволяющий пользователю переключаться между несколькими страницами контента. |
| CommandButton | `10` | Кнопка, при нажатии на которую выполняется действие. |
| Image | `11` | Элемент управления, отображающий изображение. |
| ScrollBar | `12` | Элемент управления, позволяющий пользователю прокручивать содержимое. |
| Form | `13` | Контейнер для других элементов управления. |
| ListBox | `14` | Элемент управления, отображающий список элементов. |

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

* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
