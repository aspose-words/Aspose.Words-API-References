---
title: Forms2OleControl.ChildNodes
linktitle: ChildNodes
articleTitle: ChildNodes
second_title: Aspose.Words for .NET
description: 探索 Forms2OleControl ChildNodes 属性，轻松访问和管理直接子控件，从而增强功能。
type: docs
weight: 30
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/childnodes/
---
## Forms2OleControl.ChildNodes property

获取直接子控件的集合。

```csharp
public virtual Forms2OleControlCollection ChildNodes { get; }
```

## 评论

返回`无效的`如果这个控件不能生孩子。

## 例子

展示如何验证 ActiveX 控件的属性。

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

    // 请注意，您不能为 Frame 设置 GroupName。
    checkBox.GroupName = "Aspose group name";
}
```

### 也可以看看

* class [Forms2OleControlCollection](../../forms2olecontrolcollection/)
* class [Forms2OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
