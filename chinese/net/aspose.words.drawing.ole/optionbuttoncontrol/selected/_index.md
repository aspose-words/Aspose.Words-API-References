---
title: OptionButtonControl.Selected
linktitle: Selected
articleTitle: Selected
second_title: Aspose.Words for .NET
description: 轻松管理你的 OptionButtonControl！使用简单的布尔值设置或获取其选中状态，实现无缝的用户交互。
type: docs
weight: 10
url: /zh/net/aspose.words.drawing.ole/optionbuttoncontrol/selected/
---
## OptionButtonControl.Selected property

获取或设置一个布尔值，表示[`OptionButtonControl`](../)是否被选中。

```csharp
public bool Selected { get; set; }
```

## 评论

注意，此属性允许您在一组中选择多个项目[`OptionButtonControl`](../) 相同[`GroupName`](../../forms2olecontrol/groupname/)。执行此操作时，您需要负责取消选择之前选定的项目[`OptionButtonControl`](../)已选择.

## 例子

显示如何选择单选按钮。

```csharp
Document doc = new Document(MyDir + "Radio buttons.docx");

Shape shape1 = (Shape)doc.GetChild(NodeType.Shape, 0, true);
OptionButtonControl optionButton1 = (OptionButtonControl)shape1.OleFormat.OleControl;
// 取消选择选定的第一项。
optionButton1.Selected = false;

Shape shape2 = (Shape)doc.GetChild(NodeType.Shape, 1, true);
OptionButtonControl optionButton2 = (OptionButtonControl)shape2.OleFormat.OleControl;
// 选择第二个选项按钮。
optionButton2.Selected = true;

Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton1.Type);
Assert.AreEqual(Forms2OleControlType.OptionButton, optionButton2.Type);

doc.Save(ArtifactsDir + "Shape.SelectRadioControl.docx");
```

### 也可以看看

* class [OptionButtonControl](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
