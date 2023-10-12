---
title: RevisionOptions.InsertedTextColor
second_title: Aspose.Words for .NET API Referansı
description: RevisionOptions mülk. Eklenen içerik için kullanılacak rengi belirlemeye olanak tanırInsertion . Varsayılan değerByAuthor .
type: docs
weight: 40
url: /tr/net/aspose.words.layout/revisionoptions/insertedtextcolor/
---
## RevisionOptions.InsertedTextColor property

Eklenen içerik için kullanılacak rengi belirlemeye olanak tanırInsertion . Varsayılan değer:ByAuthor .

```csharp
public RevisionColor InsertedTextColor { get; set; }
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

* enum [RevisionColor](../../revisioncolor/)
* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../revisionoptions/)
* toplantı [Aspose.Words](../../../)


