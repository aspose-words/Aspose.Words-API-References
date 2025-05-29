---
title: Forms2OleControlType Enum
linktitle: Forms2OleControlType
articleTitle: Forms2OleControlType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Ole.Forms2OleControlType 枚举，它具有一系列 Forms 2.0 控件类型，可增强文档自动化。
type: docs
weight: 1480
url: /zh/net/aspose.words.drawing.ole/forms2olecontroltype/
---
## Forms2OleControlType enumeration

枚举 Forms 2.0 控件的类型。

```csharp
public enum Forms2OleControlType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| OptionButton | `0` | 单选按钮控件。 |
| Label | `1` | 显示文本的控件。 |
| Textbox | `2` | 允许用户输入文本的控件。 |
| CheckBox | `3` | 允许用户选择或取消选择选项的控件。 |
| ToggleButton | `4` | 允许用户在两种状态之间切换的控件。 |
| SpinButton | `5` | 允许用户增加或减少值的控件。 |
| ComboBox | `6` | 允许用户从列表中选择项目的控件。 |
| Frame | `7` | 对其他控件进行分组的控件。 |
| MultiPage | `8` | 显示多页内容的控件。 |
| TabStrip | `9` | 允许用户在多个内容页面之间切换的控件。 |
| CommandButton | `10` | 点击后会触发操作的按钮。 |
| Image | `11` | 显示图像的控件。 |
| ScrollBar | `12` | 允许用户滚动浏览内容的控件。 |
| Form | `13` | 其他控件的容器。 |
| ListBox | `14` | 显示项目列表的控件。 |

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

* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
