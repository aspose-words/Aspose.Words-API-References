---
title: ReflectionFormat Class
linktitle: ReflectionFormat
articleTitle: ReflectionFormat
second_title: .NET için Aspose.Words
description: Gelişmiş nesne yansıma biçimlendirmesi için Aspose.Words.Drawing.ReflectionFormat sınıfını keşfedin. Belge tasarımınızı kusursuz entegrasyonla geliştirin!
type: docs
weight: 1570
url: /tr/net/aspose.words.drawing/reflectionformat/
---
## ReflectionFormat class

Bir nesnenin yansıma biçimlendirmesini temsil eder.

```csharp
public class ReflectionFormat
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Blur](../../aspose.words.drawing/reflectionformat/blur/) { get; set; } | Yansıma efektine uygulanan bulanıklık efektinin derecesini noktalar halinde belirten bir çift değer alır veya ayarlar. Varsayılan değer 0.0'dır. |
| [Distance](../../aspose.words.drawing/reflectionformat/distance/) { get; set; } | Yansıyan görüntünün nesneden ne kadar uzaklıkta olduğunu belirten bir double değeri alır veya ayarlar. Varsayılan değer 0.0'dır. |
| [Size](../../aspose.words.drawing/reflectionformat/size/) { get; set; } | Yansıtılan nesnenin yüzdesi olarak yansımanın boyutunu temsil eden 0,0 ile 1,0 arasında bir çift değer alır veya ayarlar. Varsayılan değer 0,0'dır. |
| [Transparency](../../aspose.words.drawing/reflectionformat/transparency/) { get; set; } | Yansıma efekti için şeffaflık derecesini temsil eden 0,0 (opak) ile 1,0 (temiz) arasında bir çift değer alır veya ayarlar. Varsayılan değer 0,0'dır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Remove](../../aspose.words.drawing/reflectionformat/remove/)() | Kaldırır`ReflectionFormat` ana nesneden. |

## Notlar

Kullanın[`Reflection`](../shapebase/reflection/) Bir nesnenin yansıma özelliklerine erişmek için özellik. Örnekleri oluşturmazsınız`ReflectionFormat` sınıfa doğrudan.

## Örnekler

Yansıma şekil efektinin nasıl etkileşime gireceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Various shapes.docx");
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

shape.Reflection.Transparency = 0.37;
shape.Reflection.Size = 0.48;
shape.Reflection.Blur = 17.5;
shape.Reflection.Distance = 9.2;

doc.Save(ArtifactsDir + "Shape.Reflection.docx");

doc = new Document(ArtifactsDir + "Shape.Reflection.docx");
shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);

ReflectionFormat reflectionFormat = shape.Reflection;

Assert.AreEqual(0.37d, reflectionFormat.Transparency, 0.01d);
Assert.AreEqual(0.48d, reflectionFormat.Size, 0.01d);
Assert.AreEqual(17.5d, reflectionFormat.Blur, 0.01d);
Assert.AreEqual(9.2d, reflectionFormat.Distance, 0.01d);

reflectionFormat.Remove();

Assert.AreEqual(0, reflectionFormat.Transparency);
Assert.AreEqual(0, reflectionFormat.Size);
Assert.AreEqual(0, reflectionFormat.Blur);
Assert.AreEqual(0, reflectionFormat.Distance);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Drawing](../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../)
