---
title: OleFormat.Clsid
linktitle: Clsid
articleTitle: Clsid
second_title: Aspose.Words for .NET
description: 发现 OleFormat Clsid 属性以轻松检索 OLE 对象的 CLSID，增强应用程序的功能和性能。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing/oleformat/clsid/
---
## OleFormat.Clsid property

获取 OLE 对象的 CLSID。

```csharp
public Guid Clsid { get; }
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

* class [OleFormat](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
