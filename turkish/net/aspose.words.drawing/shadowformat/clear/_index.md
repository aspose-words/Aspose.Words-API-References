---
title: ShadowFormat.Clear
second_title: Aspose.Words for .NET API Referansı
description: ShadowFormat yöntem. Gölge biçimini temizler.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/shadowformat/clear/
---
## ShadowFormat.Clear method

Gölge biçimini temizler.

```csharp
public void Clear()
```

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


