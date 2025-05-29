---
title: LayoutOptions.RevisionOptions
linktitle: RevisionOptions
articleTitle: RevisionOptions
second_title: .NET için Aspose.Words
description: Gelişmiş belge denetimi ve esnekliği için revizyon ayarlarına kolayca erişmek ve bunları özelleştirmek üzere LayoutOptions RevisionOptions özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words.layout/layoutoptions/revisionoptions/
---
## LayoutOptions.RevisionOptions property

Revizyon seçeneklerini alır.

```csharp
public RevisionOptions RevisionOptions { get; }
```

## Örnekler

İşlenmiş bir çıktı belgesindeki revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekle, ardından tüm revizyonların rengini yeşil yap.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Her düzeltilen satırın solunda görünen çubuğu kaldır.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;
doc.LayoutOptions.RevisionOptions.RevisionBarsPosition = HorizontalAlignment.Right;

doc.Save(ArtifactsDir + "Revision.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* class [RevisionOptions](../../revisionoptions/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
