---
title: ReflectionFormat.Blur
linktitle: Blur
articleTitle: Blur
second_title: .NET için Aspose.Words
description: Tasarımınızdaki yansımaların bulanıklık efektini kontrol etmek için ReflectionFormat Blur özelliğini ayarlayın. Görselleri hassasiyetle geliştirin; varsayılan değer 0,0'dır.
type: docs
weight: 10
url: /tr/net/aspose.words.drawing/reflectionformat/blur/
---
## ReflectionFormat.Blur property

Yansıma efektine uygulanan bulanıklık efektinin derecesini noktalar halinde belirten bir çift değer alır veya ayarlar. Varsayılan değer 0.0'dır.

```csharp
public double Blur { get; set; }
```

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

* class [ReflectionFormat](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
