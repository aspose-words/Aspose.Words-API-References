---
title: ShapeBase.AnchorLocked
linktitle: AnchorLocked
articleTitle: AnchorLocked
second_title: .NET için Aspose.Words
description: Şekiller için çapa kilitlemeyi kontrol etmek, projelerinizde tasarım kararlılığını ve esnekliği artırmak için ShapeBase AnchorLocked özelliğini keşfedin.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Şeklin bağlantısının kilitli olup olmadığını belirtir.

```csharp
public bool AnchorLocked { get; set; }
```

## Notlar

Varsayılan değer:`YANLIŞ`.

Sadece en üst seviye şekiller için etkilidir.

Bu özellik, Microsoft Word'deki şeklin çapa davranışını etkiler. Çapa kilitli olmadığında, Microsoft Word'de şekli hareket ettirmek, şeklin çapasını da hareket ettirebilir.

## Örnekler

Bir şeklin paragraf bağlantısının nasıl kilitleneceğini veya kilidinin nasıl açılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Şeklin çapa atmasını önlemek için "AnchorLocked" özelliğini "true" olarak ayarlayın
// Microsoft Word'de şekli hareket ettirirken hareket etmesini engellemek.
// Şeklin herhangi bir hareketine izin vermek için "AnchorLocked" özelliğini "false" olarak ayarlayın
// şeklin yakınına geldiği herhangi bir paragrafa da bağlantısını taşımak için.
shape.AnchorLocked = anchorLocked;

// Şeklin solunda görünür bir bağlantı sembolü yoksa,
// "Seçenekler" -> "Görüntüle" -> "Nesne Bağlantı Noktaları" yoluyla görünür bağlantıları etkinleştirmemiz gerekecek.
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
