---
title: TxtListIndentation Class
linktitle: TxtListIndentation
articleTitle: TxtListIndentation
second_title: Aspose.Words for .NET
description: Aspose.Words.Saving.TxtListIndentation sınıf. Belge dışa aktarılırken liste düzeylerinin nasıl girintileneceğini belirtirText format C#'da.
type: docs
weight: 5650
url: /tr/net/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class

Belge dışa aktarılırken liste düzeylerinin nasıl girintileneceğini belirtirText format.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Bir Belgeyi Kaydet](https://docs.aspose.com/words/net/save-a-document/) dokümantasyon makalesi.

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
| [Count](../../aspose.words.saving/txtlistindentation/count/) { get; set; } | Kaç tane olduğunu alır veya ayarlar[`Character`](./character/) bir liste düzeyi başına girinti olarak kullanılacak. Varsayılan değer 0'dır; bu, girinti olmadığı anlamına gelir. |

## Örnekler

Bir belgeyi düz metne kaydederken liste girintisinin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Üç düzeyde girintiye sahip bir liste oluşturun.
builder.ListFormat.ApplyNumberDefault();
builder.Writeln("Item 1");
builder.ListFormat.ListIndent();
builder.Writeln("Item 2");
builder.ListFormat.ListIndent(); 
builder.Write("Item 3");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirmek için.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

// Kullanılacak bir karakter atamak için "Karakter" özelliğini ayarlayın
// düz metinde liste girintisini simüle eden dolgu için.
txtSaveOptions.ListIndentation.Character = ' ';

// Kaç kez olduğunu belirtmek için "Sayma" özelliğini ayarlayın
// her liste girinti düzeyine dolgu karakteri yerleştirmek için.
txtSaveOptions.ListIndentation.Count = 3;

doc.Save(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.TxtListIndentation.txt");

Assert.AreEqual("1. Item 1\r\n" +
                "   a. Item 2\r\n" +
                "      i. Item 3\r\n", docText);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
