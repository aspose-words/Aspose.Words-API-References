---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: .NET için Aspose.Words
description: Kusursuz tasarımlar için şekillerinizin en boy oranını zahmetsizce korumak amacıyla ShapeBase AspectRatioLocked özelliğini keşfedin. Projelerinizi bugün geliştirin!
type: docs
weight: 40
url: /tr/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Şeklin en boy oranının kilitli olup olmadığını belirtir.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Notlar

Varsayılan değer, şunlara bağlıdır:[`ShapeType`](../../shapetype/) , içinImage bu`doğru` ancak diğer şekil tipleri için`YANLIŞ`.

Sadece üst seviye şekiller için etkilidir.

## Örnekler

Bir şeklin en boy oranının nasıl kilitleneceğini/kilidini nasıl açacağınızı gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir şekil ekleyin. Bu belgeyi Microsoft Word'de açarsak, şeklin üzerine sol tıklayarak şekli ortaya çıkarabiliriz
// Çevresinde, boyutunu değiştirmek için tıklayıp sürükleyebileceğiniz sekiz adet boyutlandırma tutamağı var.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Şeklin en boy oranını korumak için "AspectRatioLocked" özelliğini "true" olarak ayarlayın
// Resmin hem yüksekliğini hem de genişliğini değiştiren dört köşegen boyutlandırma tutamağından herhangi birini kullanırken.
// Yüksekliği veya genişliği değiştiren herhangi bir ortogonal boyutlandırma tutamacı kullanıldığında, en boy oranı yine de değişecektir.
// "AspectRatioLocked" özelliğini "false" olarak ayarlayın, böylece
// Tüm boyutlandırma tutamaklarıyla görüntünün en boy oranını serbestçe değiştirebilirsiniz.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
