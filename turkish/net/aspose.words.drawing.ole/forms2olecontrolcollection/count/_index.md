---
title: Forms2OleControlCollection.Count
second_title: Aspose.Words for .NET API Referansı
description: Forms2OleControlCollection mülk. Koleksiyondaki nesnelerin sayısını alır.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

Koleksiyondaki nesnelerin sayısını alır.

```csharp
public int Count { get; }
```

### Örnekler

Bir belgeye katıştırılmış bir OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Şekiller, OLE nesnelerini belgenin gövdesinde saklar ve görüntüler.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Bazı OLE denetimleri, bu belgedeki üç seçenek düğmeli gibi alt denetimler içerebilir.
Forms2OleControlCollection oleControlCollection = oleControl.ChildNodes;

Assert.AreEqual(3, oleControlCollection.Count);

Assert.AreEqual("C#", oleControlCollection[0].Caption);
Assert.AreEqual("1", oleControlCollection[0].Value);

Assert.AreEqual("Visual Basic", oleControlCollection[1].Caption);
Assert.AreEqual("0", oleControlCollection[1].Value);

Assert.AreEqual("Delphi", oleControlCollection[2].Caption);
Assert.AreEqual("0", oleControlCollection[2].Value);
```

### Ayrıca bakınız

* class [Forms2OleControlCollection](../)
* ad alanı [Aspose.Words.Drawing.Ole](../../forms2olecontrolcollection/)
* toplantı [Aspose.Words](../../../)


