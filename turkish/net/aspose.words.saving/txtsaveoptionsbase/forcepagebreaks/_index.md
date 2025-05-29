---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: .NET için Aspose.Words
description: TxtSaveOptionsBase'in ForcePageBreaks özelliği ile sayfa sonlarını kontrol edin. Sorunsuz dışa aktarımları garantileyin ve belge biçimlendirmesini zahmetsizce koruyun.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Sayfa sonlarının dışa aktarma sırasında korunup korunmayacağını belirtmenizi sağlar.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Notlar

Bu özellik yalnızca bir belgeye açıkça eklenen sayfa sonlarını etkiler. Bu özellik, MS Word'ün her sayfanın sonuna otomatik olarak eklediği sayfa sonlarıyla ilgili değildir.

## Örnekler

Bir belgeyi düz metne aktarırken sayfa sonlarının korunup korunmayacağının nasıl belirtileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Belgenin "Kaydet" komutuna geçirebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// Belgeyi düz metne nasıl kaydedeceğimizi değiştirme yöntemi.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Aspose.Words "Belge" nesnelerinin tıpkı Microsoft Word belgelerinde olduğu gibi sayfa sonları vardır.
// ".txt" gibi kaydetme biçimleri, sayfa sonları olmayan tek bir metin gövdesidir.
// '\f' karakterleri biçimindeki tüm sayfa sonlarını korumak için "ForcePageBreaks" özelliğini "true" olarak ayarlayın.
// Tüm sayfa sonlarını silmek için "ForcePageBreaks" özelliğini "false" olarak ayarlayın.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Sayfa sonları olan düz metinli bir belge yüklersek,
// "Belge" nesnesi bunları gövdeyi sayfalara bölmek için kullanacaktır.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
