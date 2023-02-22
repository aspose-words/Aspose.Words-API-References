---
title: ShapeBase.IsInline
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. Bu şeklin metinle aynı hizada olup olmadığını belirlemenin hızlı bir yolu.
type: docs
weight: 280
url: /tr/net/aspose.words.drawing/shapebase/isinline/
---
## ShapeBase.IsInline property

Bu şeklin metinle aynı hizada olup olmadığını belirlemenin hızlı bir yolu.

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

// Aşağıda, şekillerin sahip olabileceği iki sarma türü bulunmaktadır.
// 1 - Satır içi:
builder.Write("Hello world! ");
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 100);
shape.FillColor = Color.LightBlue;
builder.Write(" Hello again.");

// Satır içi şekil, metin dizileri gibi diğer paragraf öğelerinin arasında bir paragrafın içinde bulunur.
// Microsoft Word'de şekli tıklayıp herhangi bir paragrafa bir karaktermiş gibi sürükleyebiliriz.
// Şekil büyükse dikey paragraf aralığını etkiler.
// Bu şekli paragrafsız bir yere taşıyamayız.
Assert.AreEqual(WrapType.Inline, shape.WrapType);
Assert.True(shape.IsInline);

// 2 - Yüzer:
shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin ,200, 
    RelativeVerticalPosition.TopMargin ,200, 100, 100, WrapType.None);
shape.FillColor = Color.Orange;

// Bir kayan şekil, onu eklediğimiz paragrafa aittir,
// şekli tıkladığımızda görünen bir bağlantı sembolü ile belirleyebiliriz.
// Şeklin solunda görünür bir bağlantı sembolü yoksa,
// "Seçenekler" -> aracılığıyla görünür bağlantıları etkinleştirmemiz gerekecek "Ekran" -> "Nesne Çapaları".
// Microsoft Word'de bu şekli sol tıklayıp herhangi bir yere serbestçe sürükleyebiliriz.
Assert.AreEqual(WrapType.None, shape.WrapType);
Assert.False(shape.IsInline);

doc.Save(ArtifactsDir + "Shape.IsInline.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


