---
title: OleControl.Name
second_title: Aspose.Words for .NET API 参考
description: OleControl 财产. 获取或设置 ActiveX 控件的名称
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.ole/olecontrol/name/
---
## OleControl.Name property

获取或设置 ActiveX 控件的名称。

```csharp
public string Name { get; set; }
```

### 例子

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

* class [OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../olecontrol/)
* 部件 [Aspose.Words](../../../)


