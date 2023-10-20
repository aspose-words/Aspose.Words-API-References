---
title: Forms2OleControl.GroupName
linktitle: GroupName
articleTitle: GroupName
second_title: 用于 .NET 的 Aspose.Words
description: Forms2OleControl GroupName 财产. 获取或设置指定一组互斥控件的字符串 默认值为空字符串 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/groupname/
---
## Forms2OleControl.GroupName property

获取或设置指定一组互斥控件的字符串。 默认值为空字符串。

```csharp
public string GroupName { get; set; }
```

## 例子

演示如何验证 ActiveX 控件的属性。

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

    // 请注意，您不能为 Frame 设置 GroupName。
    checkBox.GroupName = "Aspose group name";
}
```

### 也可以看看

* class [Forms2OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
