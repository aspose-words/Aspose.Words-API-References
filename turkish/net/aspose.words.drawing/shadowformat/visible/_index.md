---
title: ShadowFormat.Visible
second_title: Aspose.Words for .NET API Referansı
description: ShadowFormat mülk. İadelerdoğru bu örneğe uygulanan format görünürse.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/shadowformat/visible/
---
## ShadowFormat.Visible property

İadeler`doğru` bu örneğe uygulanan format görünürse.

```csharp
public bool Visible { get; }
```

### Notlar

Beğenmedim[`Clear`](../clear/) , atama`YANLIŞ` Görünür, biçimlendirmeyi temizlemez, yalnızca şekil efektini gizler.

### Örnekler

Şeklin gölge formatıyla nasıl çalışılacağını gösterir.

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
* ad alanı [Aspose.Words.Drawing](../../shadowformat/)
* toplantı [Aspose.Words](../../../)


