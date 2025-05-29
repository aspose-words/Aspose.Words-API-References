---
title: Story.StoryType
linktitle: StoryType
articleTitle: StoryType
second_title: .NET için Aspose.Words
description: Hikayelerinizi kolayca tanımlayıp kategorilere ayırmak, organizasyonunuzu geliştirmek ve hikaye anlatma deneyiminizi iyileştirmek için StoryType özelliğini keşfedin.
type: docs
weight: 40
url: /tr/net/aspose.words/story/storytype/
---
## Story.StoryType property

Bu hikayenin türünü alır.

```csharp
public StoryType StoryType { get; }
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

* enum [StoryType](../../storytype/)
* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
