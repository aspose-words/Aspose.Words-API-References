---
title: Document.LayoutOptions
linktitle: LayoutOptions
articleTitle: LayoutOptions
second_title: .NET için Aspose.Words
description: Belgenizin düzenini etkili bir şekilde kontrol etmek için Belge Düzeni Seçenekleri özelliğini keşfedin. En iyi sunum için esnek tasarım seçeneklerinin kilidini açın.
type: docs
weight: 260
url: /tr/net/aspose.words/document/layoutoptions/
---
## Document.LayoutOptions property

Bir tane alır[`LayoutOptions`](../../../aspose.words.layout/layoutoptions/) Bu belgenin düzen sürecini kontrol etmek için seçenekleri temsil eden nesne.

```csharp
public LayoutOptions LayoutOptions { get; }
```

## Örnekler

İşlenmiş çıktı belgesinde metnin nasıl gizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Gizli metin ekleyin, ardından işlenmiş belgeden bunu çıkarmak isteyip istemediğimizi belirtin.
builder.Writeln("This text is not hidden.");
builder.Font.Hidden = true;
builder.Writeln("This text is hidden.");

doc.LayoutOptions.ShowHiddenText = showHiddenText;

doc.Save(ArtifactsDir + "Document.LayoutOptionsHiddenText.pdf");
```

İşlenmiş çıktı belgesinde paragraf işaretlerinin nasıl gösterileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
// Birkaç paragraf ekleyin, ardından paragraf sonlarını göstermek için paragraf işaretlerini etkinleştirin
// belgeyi oluştururken pilcrow (¶) sembolüyle.
builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

doc.LayoutOptions.ShowParagraphMarks = showParagraphMarks;

doc.Save(ArtifactsDir + "Document.LayoutOptionsParagraphMarks.pdf");
```

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

* class [LayoutOptions](../../../aspose.words.layout/layoutoptions/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
