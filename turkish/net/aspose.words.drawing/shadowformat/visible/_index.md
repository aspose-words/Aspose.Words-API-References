---
title: ShadowFormat.Visible
linktitle: Visible
articleTitle: Visible
second_title: .NET için Aspose.Words
description: ShadowFormat Visible özelliğini keşfedin. Biçimlendirmenizin görünür olup olmadığını kolayca kontrol edin, belgenizin görünümünü ve netliğini artırın.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

Geri Döndürür`doğru` bu örneğe uygulanan biçimlendirme görünürse.

```csharp
public bool Visible { get; }
```

## Notlar

aksine[`Clear`](../clear/) , atama`YANLIŞ`Görünür olarak ayarlamak biçimlendirmeyi temizlemez, sadece şekil efektini gizler.

## Örnekler

Şekil için gölge biçimlendirmesiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Shape stroke pattern border.docx");
Shape shape = (Shape)doc.GetChildNodes(NodeType.Shape, true)[0];

if (shape.ShadowFormat.Visible && shape.ShadowFormat.Type == ShadowType.Shadow2)
    shape.ShadowFormat.Type = ShadowType.Shadow7;

if (shape.ShadowFormat.Type == ShadowType.ShadowMixed)
    shape.ShadowFormat.Clear();
```

### Ayrıca bakınız

* class [ShadowFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
