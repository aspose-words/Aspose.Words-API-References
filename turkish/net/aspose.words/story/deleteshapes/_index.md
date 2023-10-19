---
title: Story.DeleteShapes
linktitle: DeleteShapes
articleTitle: DeleteShapes
second_title: Aspose.Words for .NET
description: Story DeleteShapes yöntem. Bu hikayenin metnindeki tüm şekilleri siler C#'da.
type: docs
weight: 70
url: /tr/net/aspose.words/story/deleteshapes/
---
## Story.DeleteShapes method

Bu hikayenin metnindeki tüm şekilleri siler.

```csharp
public void DeleteShapes()
```

## Örnekler

Bir düğümdeki tüm şekillerin nasıl kaldırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Şekil eklemek için DocumentBuilder'ı kullanın. Bu satır içi bir şekildir,
// birinci bölümün Gövdesinin alt düğümü olan bir ana Paragrafa sahiptir.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Bu Gövdenin alt paragraflarındaki tüm şekilleri silebiliriz.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Ayrıca bakınız

* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
