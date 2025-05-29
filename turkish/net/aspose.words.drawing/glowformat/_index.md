---
title: GlowFormat Class
linktitle: GlowFormat
articleTitle: GlowFormat
second_title: .NET için Aspose.Words
description: Belgelerinizi çarpıcı parıltı efektleriyle geliştirmek için Aspose.Words.Drawing.GlowFormat sınıfını keşfedin. Tasarımınızı benzersiz biçimlendirme seçenekleriyle yükseltin!
type: docs
weight: 1300
url: /tr/net/aspose.words.drawing/glowformat/
---
## GlowFormat class

Bir nesnenin parıltı biçimlendirmesini temsil eder.

```csharp
public class GlowFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Color](../../aspose.words.drawing/glowformat/color/) { get; set; } | Bir değeri alır veya ayarlarColor Parıltı efekti için rengi temsil eden nesne. Varsayılan değerBlack . |
| [Radius](../../aspose.words.drawing/glowformat/radius/) { get; set; } | Parıltı efektinin yarıçapının uzunluğunu noktalar (pt) cinsinden temsil eden bir çift değer alır veya ayarlar. Varsayılan değer 0.0'dır. |
| [Transparency](../../aspose.words.drawing/glowformat/transparency/) { get; set; } | Parıltı efekti için şeffaflık derecesini 0,0 (opak) ile 1,0 (temiz) arasında bir değer olarak alır veya ayarlar. Varsayılan değer 0,0'dır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words.drawing/glowformat/remove/)() | Kaldırır`GlowFormat` ana nesneden. |

## Notlar

Kullanın[`Glow`](../shapebase/glow/) Bir nesnenin parıltı özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`GlowFormat` sınıfa doğrudan.

## Örnekler

Parıltılı şekil efektiyle nasıl etkileşim kurulacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Glow.Color = Color.Salmon;
shape.Glow.Radius = 30;
shape.Glow.Transparency = 0.15;

doc.Save(ArtifactsDir + "Shape.Glow.docx");

doc = new Document(ArtifactsDir + "Shape.Glow.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

Assert.AreEqual(Color.FromArgb(217, 250, 128, 114).ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(30, shape.Glow.Radius);
Assert.AreEqual(0.15d, shape.Glow.Transparency, 0.01d);

shape.Glow.Remove();

Assert.AreEqual(Color.Black.ToArgb(), shape.Glow.Color.ToArgb());
Assert.AreEqual(0, shape.Glow.Radius);
Assert.AreEqual(0, shape.Glow.Transparency);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
