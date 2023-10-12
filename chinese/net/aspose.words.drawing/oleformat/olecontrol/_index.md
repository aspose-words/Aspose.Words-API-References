---
title: OleFormat.OleControl
second_title: Aspose.Words for .NET API 参考
description: OleFormat 财产. 获取OleControl对象如果此 OLE 对象是 ActiveX 控件否则此属性为 null
type: docs
weight: 60
url: /zh/net/aspose.words.drawing/oleformat/olecontrol/
---
## OleFormat.OleControl property

获取`OleControl`对象（如果此 OLE 对象是 ActiveX 控件）。否则此属性为 null。

```csharp
public OleControl OleControl { get; }
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

* class [OleControl](../../../aspose.words.drawing.ole/olecontrol/)
* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../oleformat/)
* 部件 [Aspose.Words](../../../)


