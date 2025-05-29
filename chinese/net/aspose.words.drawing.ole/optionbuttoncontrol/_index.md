---
title: OptionButtonControl Class
linktitle: OptionButtonControl
articleTitle: OptionButtonControl
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Ole.OptionButtonControl 类，它非常适合在您的应用程序中创建专属的选择选项。立即提升用户体验！
type: docs
weight: 1510
url: /zh/net/aspose.words.drawing.ole/optionbuttoncontrol/
---
## OptionButtonControl class

OptionButton 控件可在有限的一组互斥选项中实现单一选择。

```csharp
public class OptionButtonControl : MorphDataControl
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | 获取或设置控件的背景颜色。 默认值取决于控件的类型。 |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | 获取或设置控件的 Caption 属性。 默认值为空字符串。 |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | 获取直接子控件的集合。 |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | 返回`真的`如果控制处于启用状态。 |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | 获取或设置控件的前景色。 默认值取决于控件的类型。 |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | 获取或设置指定一组互斥控件的字符串。 默认值为空字符串。 |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | 获取或设置控件的高度（以点为单位）。 |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | 返回`真的`如果控件是[`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | 获取或设置 ActiveX 控件的名称。 |
| [Selected](../../aspose.words.drawing.ole/optionbuttoncontrol/selected/) { get; set; } | 获取或设置一个布尔值，表示`OptionButtonControl`是否被选中。 |
| override [Type](../../aspose.words.drawing.ole/optionbuttoncontrol/type/) { get; } | 获取 Forms 2.0 控件的类型。 |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | 获取通常代表控制状态的底层 Value 属性。 例如，选中的选项按钮的值为“1”，而未选中的选项按钮的值为“0”。 默认值为空字符串。 |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | 获取或设置控件的宽度（以点为单位）。 |

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

* class [MorphDataControl](../morphdatacontrol/)
* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
