---
title: RevisionOptions.ShowRevisionBars
second_title: Aspose.Words for .NET API Referansı
description: RevisionOptions mülk. Düzeltme çubuklarının gözden geçirilmiş içerik içeren satırların yakınında oluşturulup oluşturulmayacağını belirlemeye izin verir. Varsayılan değer Truedur.
type: docs
weight: 180
url: /tr/net/aspose.words.layout/revisionoptions/showrevisionbars/
---
## RevisionOptions.ShowRevisionBars property

Düzeltme çubuklarının, gözden geçirilmiş içerik içeren satırların yakınında oluşturulup oluşturulmayacağını belirlemeye izin verir. Varsayılan değer True'dur.

```csharp
public bool ShowRevisionBars { get; set; }
```

### Örnekler

İşlenmiş bir çıktı belgesindeki revizyonların görünümünün nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir revizyon ekleyin, ardından tüm revizyonların rengini yeşil olarak değiştirin.
builder.Writeln("This is not a revision.");
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("This is a revision.");
doc.StopTrackRevisions();
builder.Writeln("This is not a revision.");

// Revize edilen her satırın solunda görünen çubuğu kaldırın.
doc.LayoutOptions.RevisionOptions.InsertedTextColor = RevisionColor.BrightGreen;
doc.LayoutOptions.RevisionOptions.ShowRevisionBars = false;

doc.Save(ArtifactsDir + "Document.LayoutOptionsRevisions.pdf");
```

### Ayrıca bakınız

* class [RevisionOptions](../)
* ad alanı [Aspose.Words.Layout](../../revisionoptions/)
* toplantı [Aspose.Words](../../../)


