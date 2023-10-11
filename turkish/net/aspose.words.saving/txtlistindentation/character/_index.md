---
title: TxtListIndentation.Character
second_title: Aspose.Words for .NET API Referansı
description: TxtListIndentation mülk. Liste düzeylerini girintilemek için hangi karakterin kullanılacağını alır veya ayarlar. Varsayılan değer 0dır yani girinti yoktur.
type: docs
weight: 20
url: /tr/net/aspose.words.saving/txtlistindentation/character/
---
## TxtListIndentation.Character property

Liste düzeylerini girintilemek için hangi karakterin kullanılacağını alır veya ayarlar. Varsayılan değer '\0'dır, yani girinti yoktur.

```csharp
public char Character { get; set; }
```

### Örnekler

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

* class [TxtListIndentation](../)
* ad alanı [Aspose.Words.Saving](../../txtlistindentation/)
* toplantı [Aspose.Words](../../../)


