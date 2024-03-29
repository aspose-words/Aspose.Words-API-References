---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Ole.Forms2OleControlCollection 班级. 代表集合Forms2OleControl对象 在 C#.
type: docs
weight: 1120
url: /zh/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

代表集合[`Forms2OleControl`](../forms2olecontrol/)对象.

要了解更多信息，请访问[使用 Ole 对象](https://docs.aspose.com/words/net/working-with-ole-objects/)文档文章。

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | 默认构造函数。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | 获取集合中对象的计数。 |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | 获取[`Forms2OleControl`](../forms2olecontrol/)指定索引处的对象. |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | 获取枚举器。 |

## 例子

演示如何访问嵌入在文档中的 OLE 控件及其子控件。

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Shapes 在文档主体中存储和显示 OLE 对象。
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// 某些 OLE 控件可能包含子控件，例如本文档中带有三个选项按钮的控件。
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### 也可以看看

* class [Forms2OleControl](../forms2olecontrol/)
* 命名空间 [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../)
