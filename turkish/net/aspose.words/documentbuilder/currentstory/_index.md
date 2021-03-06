---
title: CurrentStory
second_title: Aspose.Words for .NET API Referansı
description: Bu DocumentBuilderda seçili olan öyküyü alır.
type: docs
weight: 70
url: /tr/net/aspose.words/documentbuilder/currentstory/
---
## DocumentBuilder.CurrentStory property

Bu DocumentBuilder'da seçili olan öyküyü alır.

```csharp
public Story CurrentStory { get; }
```

### Örnekler

Bir belge oluşturucunun mevcut öyküsüyle nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Öykü, Gövde gibi alt Paragraf düğümleri olan bir düğüm türüdür.
Assert.AreEqual(builder.CurrentStory, doc.FirstSection.Body);
Assert.AreEqual(builder.CurrentStory, builder.CurrentParagraph.ParentNode);
Assert.AreEqual(StoryType.MainText, builder.CurrentStory.StoryType);

builder.CurrentStory.AppendParagraph("Text added to current Story.");

// Bir Öykü ayrıca tablolar içerebilir.
Table table = builder.StartTable();
builder.InsertCell();
builder.Write("Row 1, cell 1");
builder.InsertCell();
builder.Write("Row 1, cell 2");
builder.EndTable();

Assert.IsTrue(builder.CurrentStory.Tables.Contains(table));
```

### Ayrıca bakınız

* class [Story](../../story)
* class [DocumentBuilder](../../documentbuilder)
* ad alanı [Aspose.Words](../../documentbuilder)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
