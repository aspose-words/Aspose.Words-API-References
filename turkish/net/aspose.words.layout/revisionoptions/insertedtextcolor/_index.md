---
title: RevisionOptions.InsertedTextColor
linktitle: InsertedTextColor
articleTitle: InsertedTextColor
second_title: .NET için Aspose.Words
description: RevisionOptions InsertedTextColor özelliğiyle düzenleme deneyiminizi özelleştirin ve eklenen içerik için benzersiz renkler ayarlayın. Varsayılan, ByAuthor.
type: docs
weight: 60
url: /tr/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Eklenen içerik için kullanılacak rengin belirtilmesine olanak tanırInsertion . Varsayılan değerByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
