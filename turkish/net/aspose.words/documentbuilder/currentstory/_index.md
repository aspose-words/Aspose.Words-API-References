---
title: DocumentBuilder.CurrentStory
linktitle: CurrentStory
articleTitle: CurrentStory
second_title: .NET için Aspose.Words
description: Seçili hikayeye etkin bir şekilde erişmek ve onu yönetmek için DocumentBuilder CurrentStory özelliğini keşfedin; böylece belge düzenleme deneyiminizi geliştirin.
type: docs
weight: 70
url: /tr/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Bu bölümde şu anda seçili olan hikayeyi alır[`DocumentBuilder`](../) .

```csharp
public Story CurrentStory { get; }
```

## Örnekler

Belge oluşturucunun mevcut hikayesiyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Hikaye, Gövde gibi alt Paragraf düğümlerine sahip bir düğüm türüdür.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// Bir Hikaye tablolar da içerebilir.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Ayrıca bakınız

* class [Story](../../story/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
