---
title: Forms2OleControlCollection Class
linktitle: Forms2OleControlCollection
articleTitle: Forms2OleControlCollection
second_title: .NET için Aspose.Words
description: Belge işlemede Forms2OleControl nesnelerini etkili bir şekilde yönetmeniz için çözümünüz olan Aspose.Words.Drawing.Ole.Forms2OleControlCollection sınıfını keşfedin.
type: docs
weight: 1470
url: /tr/net/aspose.words.drawing.ole/forms2olecontrolcollection/
---
## Forms2OleControlCollection class

koleksiyonunu temsil eder[`Forms2OleControl`](../forms2olecontrol/) nesneler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Ole Nesneleriyle Çalışma](https://docs.aspose.com/words/net/working-with-ole-objects/) belgeleme makalesi.

```csharp
public class Forms2OleControlCollection : IEnumerable<Forms2OleControl>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Forms2OleControlCollection](forms2olecontrolcollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.drawing.ole/forms2olecontrolcollection/count/) { get; } | Koleksiyondaki nesnelerin sayısını alır. |
| [Item](../../aspose.words.drawing.ole/forms2olecontrolcollection/item/) { get; } | Alır[`Forms2OleControl`](../forms2olecontrol/) belirtilen bir dizindeki nesne. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.ole/forms2olecontrolcollection/getenumerator/)() | Numaratör alır. |

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

* class [Forms2OleControl](../forms2olecontrol/)
* ad alanı [Aspose.Words.Drawing.Ole](../../aspose.words.drawing.ole/)
* toplantı [Aspose.Words](../../)
