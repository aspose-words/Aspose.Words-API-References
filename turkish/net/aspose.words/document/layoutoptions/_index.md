---
title: Document.LayoutOptions
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. DüzenSeçenekleri bu belgenin yerleşim sürecini denetleme seçeneklerini temsil eden nesne.
type: docs
weight: 230
url: /tr/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

**DüzenSeçenekleri** bu belgenin yerleşim sürecini denetleme seçeneklerini temsil eden nesne.

```csharp
public LayoutOptions LayoutOptions { get; }
```

### Örnekler

İşlenmiş bir çıktı belgesindeki metnin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Gizli metni ekleyin, ardından onu işlenmiş bir belgeden çıkarmak isteyip istemediğimizi belirtin.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

İşlenmiş bir çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Bazı paragraflar ekleyin, ardından paragrafların sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluşturduğumuzda bir pilcrow (¶) sembolü ile.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


