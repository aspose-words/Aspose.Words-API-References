---
title: Story.StoryType
second_title: Aspose.Words for .NET API Referansı
description: Story mülk. Bu hikayenin türünü alır.
type: docs
weight: 40
url: /tr/net/aspose.words/story/storytype/
---
## Story.StoryType property

Bu hikayenin türünü alır.

```csharp
public StoryType StoryType { get; }
```

### Örnekler

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

* enum [StoryType](../../storytype/)
* class [Story](../)
* ad alanı [Aspose.Words](../../story/)
* toplantı [Aspose.Words](../../../)


