---
title: ShapeBase.MarkupLanguage
linktitle: MarkupLanguage
articleTitle: MarkupLanguage
second_title: Aspose.Words for .NET
description: 探索 ShapeBase MarkupLanguage 属性，增强图形对象管理。立即解锁无缝集成，提升设计效率！
type: docs
weight: 410
url: /zh/net/aspose.words.drawing/shapebase/markuplanguage/
---
## ShapeBase.MarkupLanguage property

获取此图形对象使用的标记语言。

```csharp
public ShapeMarkupLanguage MarkupLanguage { get; }
```

## 例子

展示如何验证形状的大小和标记语言。

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
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
