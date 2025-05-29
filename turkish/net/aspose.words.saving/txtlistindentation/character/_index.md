---
title: TxtListIndentation.Character
linktitle: Character
articleTitle: Character
second_title: .NET için Aspose.Words
description: Liste girintisini tercih ettiğiniz karakterle özelleştirmek için TxtListIndentation özelliğini keşfedin. Okunabilirliği ve görsel çekiciliği zahmetsizce artırın!
type: docs
weight: 20
url: /tr/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

Liste düzeylerini girintilemek için hangi karakterin kullanılacağını alır veya ayarlar. Varsayılan değer '\0'dır, yani girinti yoktur.

```csharp
public char Character { get; set; }
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

* class [TxtListIndentation](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
