---
title: ShapeBase.IsInline
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Bu şeklin metinle satır içi olarak konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu.
type: docs
weight: 290
url: /tr/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Bu şeklin metinle satır içi olarak konumlandırılıp konumlandırılmadığını belirlemenin hızlı bir yolu.

```csharp
public bool IsInline { get; }
```

### Notlar

Yalnızca üst düzey şekiller için etkilidir.

### Örnekler

Bir şeklin satır içi mi yoksa kayan mı olduğunun nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Aşağıda şekillerin sahip olabileceği iki sarma türü verilmiştir.
// 1 - Satır içi:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Satır içi şekil, paragrafın içinde, metin dizileri gibi diğer paragraf öğelerinin arasında yer alır.
// Microsoft Word'de şekle tıklayıp herhangi bir paragrafa sanki bir karaktermiş gibi sürükleyebiliriz.
// Şeklin büyük olması dikey paragraf aralığını etkileyecektir.
// Bu şekli paragrafsız bir yere taşıyamayız.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Kayan:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Kayan bir şekil onu eklediğimiz paragrafa aittir,
// bunu şekle tıkladığımızda beliren bağlantı sembolüyle belirleyebiliriz.
// Şeklin solunda görünür bir bağlantı sembolü yoksa,
// "Seçenekler" aracılığıyla görünür bağlantıları etkinleştirmemiz gerekecek -> "Ekran" -> "Nesne Bağlantıları".
// Microsoft Word'de bu şekle sol tıklayıp serbestçe herhangi bir yere sürükleyebiliriz.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


