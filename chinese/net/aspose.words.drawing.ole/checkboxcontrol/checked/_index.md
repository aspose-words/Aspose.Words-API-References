---
title: CheckBoxControl.Checked
linktitle: Checked
articleTitle: Checked
second_title: Aspose.Words for .NET
description: 探索 CheckBoxControl 的 Checked 属性，使用简单的布尔值轻松管理复选框状态。默认值为 false，以实现最佳控制。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.ole/checkboxcontrol/checked/
---
## CheckBoxControl.Checked property

获取或设置一个布尔值，表示[`CheckBoxControl`](../)是否检查。 默认值为`错误的`.

```csharp
public bool Checked { get; set; }
```

## 例子

显示如何改变 CheckBox 控件的状态。

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
CheckBoxControl checkBoxControl = (CheckBoxControl)shape.OleFormat.OleControl;
checkBoxControl.Checked = true;

Assert.AreEqual(true, checkBoxControl.Checked);
Assert.AreEqual(Forms2OleControlType.CheckBox, checkBoxControl.Type);
```

### 也可以看看

* class [CheckBoxControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
