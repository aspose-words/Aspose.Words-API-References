---
title: Forms2OleControlCollection.Count
linktitle: Count
articleTitle: Count
second_title: .NET için Aspose.Words
description: Gelişmiş veri yönetimi için koleksiyonunuzdaki nesnelerin toplam sayısını kolayca almak üzere Forms2OleControlCollection Count özelliğini keşfedin.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing.ole/forms2olecontrolcollection/count/
---
## Forms2OleControlCollection.Count property

Koleksiyondaki nesnelerin sayısını alır.

```csharp
public int Count { get; }
```

## Örnekler

Bir belgeye gömülü bir OLE denetimine ve onun alt denetimlerine nasıl erişileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "OLE ActiveX controls.docm");

// Şekiller, OLE nesnelerini belgenin gövdesinde depolar ve görüntüler.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual("6e182020-f460-11ce-9bcd-00aa00608e01", shape.OleFormat.Clsid.ToString());

Forms2OleControl oleControl = (Forms2OleControl)shape.OleFormat.OleControl;

// Bazı OLE denetimleri, bu belgedeki üç seçenek düğmesine sahip denetim gibi, alt denetimler içerebilir.
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
* ad alanı [Aspose.Words.Drawing.Ole](../../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../../)
