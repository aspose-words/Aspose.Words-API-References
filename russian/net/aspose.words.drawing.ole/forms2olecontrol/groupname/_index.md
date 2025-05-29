---
title: Forms2OleControl.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: Aspose.Words для .NET
description: Узнайте, как свойство Forms2OleControl GroupName улучшает пользовательский опыт, легко управляя взаимоисключающими элементами управления. Узнайте больше!
type: docs
weight: 60
url: /ru/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

Возвращает или задает строку, которая определяет группу взаимоисключающих элементов управления. Значением по умолчанию является пустая строка.

```csharp
public string GroupName { get; set; }
```

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

* class [Forms2OleControl](../)
* пространство имен [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* сборка [Aspose.Words](../../../)
