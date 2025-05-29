---
title: CheckBoxControl.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: 探索 Forms 2.0 的 CheckBoxControl Type 属性，解锁多种控制选项以增强应用程序的功能。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.ole/checkboxcontrol/type/
---
## CheckBoxControl.Type property

获取 Forms 2.0 控件的类型。

```csharp
public override Forms2OleControlType Type { get; }
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

* enum [Forms2OleControlType](../../forms2olecontroltype/)
* class [CheckBoxControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
