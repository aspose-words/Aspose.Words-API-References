---
title: TxtSaveOptions.ListIndentation
linktitle: ListIndentation
articleTitle: ListIndentation
second_title: .NET için Aspose.Words
description: Gelişmiş okunabilirlik için liste girintisini özelleştiren TxtSaveOptions ListIndentation özelliğini keşfedin. Karakterleri ve seviyeleri zahmetsizce kontrol edin!
type: docs
weight: 30
url: /tr/net/aspose.words.saving/txtsaveoptions/listindentation/
---
## TxtSaveOptions.ListIndentation property

Bir tane alır[`TxtListIndentation`](../../txtlistindentation/)liste seviyelerinin girintisi için hangi karakter ve kaç tane kullanılacağını belirten nesne. Varsayılan olarak '\0' karakterinin sayısı sıfırdır, bu girinti olmadığı anlamına gelir.

```csharp
public TxtListIndentation ListIndentation { get; }
```

## Örnekler

Bir belgeyi düz metne kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üç düzeyde girintiye sahip bir liste oluştur.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Kullanılacak bir karakter atamak için "Karakter" özelliğini ayarlayın
// düz metinde liste girintisini simüle eden dolgu için.
txtSaveOptions.ListIndentation.Character = ' ';

// "Count" özelliğini, kaç kez olacağını belirtmek için ayarlayın
// her liste girinti düzeyi için dolgu karakterini yerleştirmek için.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");
string newLine= Environment.NewLine;

Assert.AreEqual($"1. Item 1{newLine}" +
                $"   a. Item 2{newLine}" +
                $"      i. Item 3{newLine}", docText);
```

### Ayrıca bakınız

* class [TxtListIndentation](../../txtlistindentation/)
* class [TxtSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
