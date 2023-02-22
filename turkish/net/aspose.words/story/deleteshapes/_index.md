---
title: Story.DeleteShapes
second_title: Aspose.Words for .NET API Referansı
description: Story yöntem. Bu hikayenin metninden tüm şekilleri siler.
type: docs
weight: 70
url: /tr/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Bu hikayenin metninden tüm şekilleri siler.

```csharp
public void DeleteShapes()
```

### Örnekler

Bir düğümden tüm şekillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Şekil eklemek için DocumentBuilder kullanın. Bu bir satır içi şekil,
// birinci bölümün Gövdesinin alt düğümü olan bir üst Paragrafı olan.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Bu Body'nin alt paragraflarından tüm şekilleri silebiliriz.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* class [Story](../)
* ad alanı [Aspose.Words](../../story/)
* toplantı [Aspose.Words](../../../)


