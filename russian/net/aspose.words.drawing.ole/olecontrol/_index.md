---
title: OleControl Class
linktitle: OleControl
articleTitle: OleControl
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Drawing.Ole.OleControl, который позволяет легко интегрировать элементы управления OLE ActiveX в ваши приложения для улучшения функциональности.
type: docs
weight: 1500
url: /ru/net/aspose.words.drawing.ole/olecontrol/
---
## OleControl class

Представляет элемент управления OLE ActiveX.

Чтобы узнать больше, посетите[Работа с Ole-объектами](https://docs.aspose.com/words/net/working-with-ole-objects/) документальная статья.

```csharp
public class OleControl
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | Возврат`истинный` если контроль - это[`Forms2OleControl`](../forms2olecontrol/) . |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | Возвращает или задает имя элемента управления ActiveX. |

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

* пространство имен [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../)
