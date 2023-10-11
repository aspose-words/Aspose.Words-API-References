---
title: Class Forms2OleControl
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Ole.Forms2OleControl 班级. 代表 Microsoft Forms 2.0 OLE 控件
type: docs
weight: 1110
url: /zh/net/aspose.words.drawing.ole/forms2olecontrol/
---
## Forms2OleControl class

代表 Microsoft Forms 2.0 OLE 控件。

要了解更多信息，请访问[使用 Ole 对象](https://docs.aspose.com/words/net/working-with-ole-objects/)文档文章。

```csharp
public abstract class Forms2OleControl : OleControl
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Caption](../../aspose.words.drawing.ole/forms2olecontrol/caption/) { get; } | 获取控件的 Caption 属性。默认值为空字符串。 |
| virtual [ChildNodes](../../aspose.words.drawing.ole/forms2olecontrol/childnodes/) { get; } | 获取直接子控件的集合。 |
| [Enabled](../../aspose.words.drawing.ole/forms2olecontrol/enabled/) { get; } | 返回`真的`如果控制处于启用状态。 |
| [GroupName](../../aspose.words.drawing.ole/forms2olecontrol/groupname/) { get; set; } | 获取或设置指定一组互斥控件的字符串。 默认值为空字符串。 |
| [IsForms2OleControl](../../aspose.words.drawing.ole/olecontrol/isforms2olecontrol/) { get; } | 返回`真的`如果控制是`Forms2OleControl`. |
| [Name](../../aspose.words.drawing.ole/olecontrol/name/) { get; set; } | 获取或设置 ActiveX 控件的名称。 |
| abstract [Type](../../aspose.words.drawing.ole/forms2olecontrol/type/) { get; } | 获取 Forms 2.0 控件的类型。 |
| [Value](../../aspose.words.drawing.ole/forms2olecontrol/value/) { get; } | 获取通常表示控件状态的基础 Value 属性。 例如，选中的选项按钮具有“1”值，而未选中的值为“0”。 默认值为空字符串。 |

### 例子

演示如何验证 ActiveX 控件的属性。

```csharp
Document doc = new Document(MyDir + "ActiveX controls.docx");

Shape shape = (Shape) doc.GetChild(NodeType.Shape, 0, true);
OleControl oleControl = shape.OleFormat.OleControl;

Assert.AreEqual("CheckBox1", oleControl.Name);

if (oleControl.IsForms2OleControl)
{
    Forms2OleControl checkBox = (Forms2OleControl) oleControl;
    Assert.AreEqual("Первый", checkBox.Caption);
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

* class [OleControl](../olecontrol/)
* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)


