---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: .NET için Aspose.Words
description: Kusursuz Metin biçimi dışa aktarımları için liste girinti düzeylerini özelleştirmek üzere Aspose.Words.Saving.TxtListIndentation sınıfını keşfedin. Belge biçimlendirmenizi geliştirin!
type: docs
weight: 6450
url: /tr/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Belge dışa aktarılırken liste düzeylerinin nasıl girintilendirileceğini belirtirText biçim.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) belgeleme makalesi.

```csharp
public class TxtListIndentation
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [TxtListIndentation](txtlistindentation/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Character](../../aspose.words.saving/txtlistindentation/character/) { get; set; } | Liste düzeylerini girintilemek için hangi karakterin kullanılacağını alır veya ayarlar. Varsayılan değer '\0'dır, yani girinti yoktur. |
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Kaç tane alır veya ayarlar[`Character`](./character/)bir liste düzeyi başına girinti olarak kullanmak için. Varsayılan değer 0'dır, bu girinti olmadığı anlamına gelir. |

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

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
