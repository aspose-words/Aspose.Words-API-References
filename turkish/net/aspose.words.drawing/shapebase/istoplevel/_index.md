---
title: ShapeBase.IsTopLevel
second_title: Aspose.Words for .NET API Referansı
description: ShapeBase mülk. İadelerdoğrubu şekil bir grup şeklinin alt öğesi değilse.
type: docs
weight: 350
url: /tr/net/aspose.words.drawing/shapebase/istoplevel/
---
## ShapeBase.IsTopLevel property

İadeler`doğru`bu şekil bir grup şeklinin alt öğesi değilse.

```csharp
public bool IsTopLevel { get; }
```

### Örnekler

Bir şeklin grup şeklinin parçası olup olmadığının nasıl anlaşılacağını gösterir.

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
* ad alanı [Aspose.Words.Drawing](../../shapebase/)
* toplantı [Aspose.Words](../../../)


