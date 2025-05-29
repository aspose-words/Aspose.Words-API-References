---
title: Forms2OleControl.Value
linktitle: Value
articleTitle: Value
second_title: Aspose.Words for .NET
description: 探索 Forms2OleControl 的 Value 属性，反映控件状态。轻松管理选项按钮的值，1 表示选中，0 表示未选中。简化您的编码！
type: docs
weight: 90
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

获取通常代表控制状态的底层 Value 属性。 例如，选中的选项按钮的值为“1”，而未选中的选项按钮的值为“0”。 默认值为空字符串。

```csharp
public string Value { get; }
```

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

* class [Forms2OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
