---
title: Forms2OleControl.Value
second_title: Aspose.Words for .NET API 参考
description: Forms2OleControl 财产. 获取通常表示控件状态的底层 Value 属性 例如选中的选项按钮具有1值而未选中的具有0 默认值为空字符串
type: docs
weight: 60
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/value/
---
## Forms2OleControl.Value property

获取通常表示控件状态的底层 Value 属性。 例如，选中的选项按钮具有“1”值，而未选中的具有“0”。 默认值为空字符串。

```csharp
public string Value { get; }
```

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

* class [Forms2OleControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../forms2olecontrol/)
* 部件 [Aspose.Words](../../../)


