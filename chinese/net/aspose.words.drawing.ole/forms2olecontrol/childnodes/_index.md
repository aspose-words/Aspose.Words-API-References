---
title: Forms2OleControl.ChildNodes
second_title: Aspose.Words for .NET API 参考
description: Forms2OleControl 财产. 获取直接子控件的集合
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

获取直接子控件的集合。

```csharp
public Forms2OleControlCollection ChildNodes { get; }
```

### 评论

退货 **无效的**如果这个控件不能有孩子。

### 例子

演示如何验证 ActiveX 控件的属性。

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual(null, oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
    Assert.AreEqual("0", checkBox.Value);
    Assert.AreEqual(true, checkBox.Enabled);
    Assert.AreEqual(Forms2OleControlType.CheckBox, checkBox.Type);
    Assert.AreEqual(null, checkBox.ChildNodes);
}
```

### 也可以看看

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* 部件 [Aspose.Words](../../../)


