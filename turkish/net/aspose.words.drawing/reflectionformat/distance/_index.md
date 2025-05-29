---
title: ReflectionFormat.Distance
linktitle: Distance
articleTitle: Distance
second_title: .NET için Aspose.Words
description: ReflectionFormat Distance özelliğini keşfedin, çarpıcı görsel efektler için yansıyan görüntünüzün noktasal ayrımını kolayca ayarlayın. Varsayılan değer 0.0'dır.
type: docs
weight: 20
url: /tr/net/aspose.words.drawing/reflectionformat/distance/
---
## ReflectionFormat.Distance property

Yansıyan görüntünün nesneden ne kadar uzaklıkta olduğunu belirten bir double değeri alır veya ayarlar. Varsayılan değer 0.0'dır.

```csharp
public double Distance { get; set; }
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
