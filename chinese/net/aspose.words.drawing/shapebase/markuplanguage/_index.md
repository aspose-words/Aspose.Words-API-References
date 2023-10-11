---
title: ShapeBase.MarkupLanguage
second_title: Aspose.Words for .NET API 参考
description: ShapeBase 财产. 获取用于此图形对象的 MarkupLanguage
type: docs
weight: 390
url: /zh/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

获取用于此图形对象的 MarkupLanguage。

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

### 例子

演示如何验证形状的大小和标记语言。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");

Assert.AreEqual(ShapeMarkupLanguage.Dml, shape.MarkupLanguage);
Assert.AreEqual(new SizeF(300, 300), shape.SizeInPoints);
```

### 也可以看看

* enum [ShapeMarkupLanguage](../../shapemarkuplanguage/)
* class [ShapeBase](../)
* 命名空间 [Aspose.Words.Drawing](../../shapebase/)
* 部件 [Aspose.Words](../../../)


