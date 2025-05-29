---
title: ShapeBase.IsTopLevel
linktitle: IsTopLevel
articleTitle: IsTopLevel
second_title: .NET için Aspose.Words
description: ShapeBase IsTopLevel'ı keşfedin. Bir şeklin tek başına durup durmadığını hızla doğrulayın ve verimli grup yönetimiyle tasarım iş akışınızı geliştirin.
type: docs
weight: 370
url: /tr/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

Geri Döndürür`doğru` eğer bu şekil bir grup şeklinin çocuğu değilse.

```csharp
public bool IsTopLevel { get; }
```

## Örnekler

Bir şeklin bir grup şeklinin parçası olup olmadığının nasıl anlaşılacağını gösterir.

```csharp
Document doc = new Document();

Shape shape = new Shape(doc, ShapeType.Rectangle);
shape.Width = 200;
shape.Height = 200;
shape.WrapType = WrapType.None;

// Bir şekil varsayılan olarak herhangi bir grup şeklinin parçası değildir ve bu nedenle "IsTopLevel" özelliği "true" olarak ayarlanmıştır.
Assert.True(shape.IsTopLevel);

GroupShape group = new GroupShape(doc);
group.AppendChild(shape);

// Bir şekli bir grup şekline asimile ettiğimizde, "IsTopLevel" özelliği "false" olarak değişir.
Assert.False(shape.IsTopLevel);
```

### Ayrıca bakınız

* class [ShapeBase](../)
* ad alanı [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* toplantı [Aspose.Words](../../../)
