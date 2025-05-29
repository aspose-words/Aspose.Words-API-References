---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: .NET için Aspose.Words
description: DeleteShapes yöntemiyle hikaye metninizden tüm şekilleri zahmetsizce kaldırın. İçeriğinizi basitleştirin ve netliği bugün artırın!
type: docs
weight: 70
url: /tr/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Bu hikayenin metninden tüm şekilleri siler.

```csharp
public void DeleteShapes()
```

## Örnekler

Bir düğümden tüm şekillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir şekil eklemek için bir DocumentBuilder kullanın. Bu bir satır içi şekildir,
// ilk bölümün Gövdesinin bir alt düğümü olan bir ana Paragrafı vardır.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Bu Gövdenin alt paragraflarından tüm şekilleri silebiliriz.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
