---
title: ShapeBase.AnchorLocked
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Şeklin bağlantısının kilitli olup olmadığını belirtir.
type: docs
weight: 30
url: /tr/net/aspose.words.drawing/shapebase/anchorlocked/
---
## ShapeBase.AnchorLocked property

Şeklin bağlantısının kilitli olup olmadığını belirtir.

```csharp
public bool AnchorLocked { get; set; }
```

### Notlar

Varsayılan değer **yanlış**.

Yalnızca üst düzey şekiller için etkilidir.

Bu özellik, Microsoft Word'deki şeklin çapasının davranışını etkiler. Bağlantı kilitli olmadığında, şekli Microsoft Word'de hareket ettirmek şeklin çapasını da taşıyabilir.

### Örnekler

Bir şeklin paragraf bağlantısının nasıl kilitleneceğini veya kilidinin açılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

builder.Write("Our shape will have an anchor attached to this paragraph.");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 200, 160);
shape.WrapType = WrapType.None;
builder.InsertBreak(BreakType.ParagraphBreak);

builder.Writeln("Hello again!");

// Şeklin çapasını önlemek için "AnchorLocked" özelliğini "true" olarak ayarlayın
// Microsoft Word'de şekli taşırken hareket etmekten.
// Şeklin herhangi bir hareketine izin vermek için "AnchorLocked" özelliğini "false" olarak ayarlayın
// ayrıca çapasını şeklin yakın olduğu diğer paragraflara taşımak için.
shape.AnchorLocked = anchorLocked;

// Şeklin solunda görünür bir bağlantı sembolü yoksa,
// "Seçenekler" -> aracılığıyla görünür bağlantıları etkinleştirmemiz gerekecek "Ekran" -> "Nesne Çapaları".
doc.Save(ArtifactsDir + "Shape.AnchorLocked.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


