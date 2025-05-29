---
title: CheckBoxControl Class
linktitle: CheckBoxControl
articleTitle: CheckBoxControl
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Ole.CheckBoxControl 类，轻松切换复选框值并通过无缝集成增强文档自动化。
type: docs
weight: 1440
url: /zh/net/aspose.words.drawing.ole/checkboxcontrol/
---
## CheckBoxControl class

CheckBox 控件切换一个值。

```csharp
public class CheckBoxControl : MorphDataControl
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [BackColor](../../aspose.words.drawing.ole/forms2olecontrol/backcolor/) { get; set; } | 获取或设置控件的背景颜色。 默认值取决于控件的类型。 |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; set; } | 获取或设置控件的 Caption 属性。 默认值为空字符串。 |
| [Checked](../../aspose.words.drawing.ole/checkboxcontrol/checked/) { get; set; } | 获取或设置一个布尔值，表示`CheckBoxControl`是否检查。 默认值为`错误的`. |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | 获取直接子控件的集合。 |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | 返回`真的`如果控制处于启用状态。 |
| [ForeColor](../../aspose.words.drawing.ole/forms2olecontrol/forecolor/) { get; set; } | 获取或设置控件的前景色。 默认值取决于控件的类型。 |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | 获取或设置指定一组互斥控件的字符串。 默认值为空字符串。 |
| [Height](../../aspose.words.drawing.ole/forms2olecontrol/height/) { get; set; } | 获取或设置控件的高度（以点为单位）。 |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | 返回`真的`如果控件是[`Forms2OleControl`](../forms2olecontrol/). |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | 获取或设置 ActiveX 控件的名称。 |
| override [Type](../../aspose.words.drawing.ole/checkboxcontrol/type/) { get; } | 获取 Forms 2.0 控件的类型。 |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | 获取通常代表控制状态的底层 Value 属性。 例如，选中的选项按钮的值为“1”，而未选中的选项按钮的值为“0”。 默认值为空字符串。 |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | 获取或设置控件的宽度（以点为单位）。 |

## 评论

它有三种可能的状态：选中、清除、既未选中也未清除， 表示开启和关闭状态的组合。

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

* class [MorphDataControl](../morphdatacontrol/)
* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
