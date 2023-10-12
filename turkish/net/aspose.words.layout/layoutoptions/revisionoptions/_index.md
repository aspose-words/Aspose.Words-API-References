---
title: LayoutOptions.RevisionOptions
second_title: Aspose.Words for .NET API Referansı
description: LayoutOptions mülk. Revizyon seçeneklerini alır.
type: docs
weight: 70
url: /tr/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Revizyon seçeneklerini alır.

```csharp
public RevisionOptions RevisionOptions { get; }
```

### Örnekler

İşlenmiş bir çıktı belgesindeki düzeltmelerin görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşil olarak değiştirin.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Düzenlenen her satırın solunda görünen çubuğu kaldırın.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../layoutoptions/)
* toplantı [Aspose.Words](../../../)


