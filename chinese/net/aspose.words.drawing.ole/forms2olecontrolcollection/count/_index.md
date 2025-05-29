---
title: Forms2OleControlCollection.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words for .NET
description: 探索 Forms2OleControlCollection Count 属性，轻松检索集合中的对象总数，从而增强数据管理。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

获取集合中的对象数量。

```csharp
public int Count { get; }
```

## 例子

演示如何访问文档中嵌入的 OLE 控件及其子控件。

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// 形状在文档主体中存储和显示 OLE 对象。
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

* class [Forms2OleControlCollection](../)
* 命名空间 [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* 部件 [Aspose.Words](../../../)
