---
title: ShapeBase.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: .NET için Aspose.Words
description: ShapeBase'in gizli özelliğiyle şekil görünürlüğünü kontrol edin. Gelişmiş tasarım esnekliği için görünür ve gizli arasında kolayca geçiş yapın.
type: docs
weight: 230
url: /tr/net/aspose.words.drawing/shapebase/hidden/
---
## ShapeBase.Hidden property

Şeklin görünür olup olmadığını belirten bir Boole değeri alır veya ayarlar.

```csharp
public bool Hidden { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ` .

## Örnekler

Şeklin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Shadow color.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
if (!shape.Hidden)
    shape.Hidden = true;

doc.Save(ArtifactsDir + "Shape.Hidden.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
