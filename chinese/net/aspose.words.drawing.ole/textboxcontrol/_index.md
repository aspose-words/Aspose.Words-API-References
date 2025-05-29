---
title: TextBoxControl Class
linktitle: TextBoxControl
articleTitle: TextBoxControl
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Ole.TextBoxControl 类，轻松显示根据数据或用户输入整理的文本。立即增强您的文档管理！
type: docs
weight: 1520
url: /zh/net/aspose.words.drawing.ole/textboxcontrol/
---
## TextBoxControl class

TextBox 控件显示来自有组织的数据集或用户输入的文本。

```csharp
public class TextBoxControl : MorphDataControl
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
| [Text](../../aspose.words.drawing.ole/textboxcontrol/text/) { get; set; } | 获取或设置控件的文本。 |
| override [Type](../../aspose.words.drawing.ole/textboxcontrol/type/) { get; } | 获取 Forms 2.0 控件的类型。 |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | 获取通常代表控制状态的底层 Value 属性。 例如，选中的选项按钮的值为“1”，而未选中的选项按钮的值为“0”。 默认值为空字符串。 |
| [Width](../../aspose.words.drawing.ole/forms2olecontrol/width/) { get; set; } | 获取或设置控件的宽度（以点为单位）。 |

## 例子

展示如何更改 TextBox OLE 控件的文本。

```csharp
Document doc = new Document(MyDir + "Textbox control.docm");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
TextBoxControl textBoxControl = (TextBoxControl)shape.OleFormat.OleControl;
Assert.AreEqual("Aspose.Words test", textBoxControl.Text);

textBoxControl.Text = "Updated text";
Assert.AreEqual("Updated text", textBoxControl.Text);
Assert.AreEqual(Forms2OleControlType.Textbox, textBoxControl.Type);
```

### 也可以看看

* class [MorphDataControl](../morphdatacontrol/)
* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
