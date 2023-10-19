---
title: TxtSaveOptionsBase.ForcePageBreaks
linktitle: ForcePageBreaks
articleTitle: ForcePageBreaks
second_title: Aspose.Words for .NET
description: TxtSaveOptionsBase ForcePageBreaks mülk. Dışa aktarma sırasında sayfa sonlarının korunup korunmayacağını belirtmenize olanak tanır C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/
---
## TxtSaveOptionsBase.ForcePageBreaks property

Dışa aktarma sırasında sayfa sonlarının korunup korunmayacağını belirtmenize olanak tanır.

Varsayılan değer:`YANLIŞ`.

```csharp
public bool ForcePageBreaks { get; set; }
```

## Notlar

Bu özellik yalnızca belgeye açıkça eklenen sayfa sonlarını etkiler. MS Word'ün her sayfanın sonuna otomatik olarak eklediği sayfa sonlarıyla ilgisi yoktur.

## Örnekler

Bir belgeyi düz metne dışa aktarırken sayfa sonlarının korunup korunmayacağının nasıl belirleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page 3");

// Belgenin "Kaydet" kısmına iletebileceğimiz bir "TxtSaveOptions" nesnesi oluşturun
// belgeyi düz metne kaydetme şeklimizi değiştirme yöntemi.
TxtSaveOptions saveOptions = new TxtSaveOptions();

// Aspose.Words "Document" nesnelerinin tıpkı Microsoft Word belgelerinde olduğu gibi sayfa sonları vardır.
// ".txt" gibi kaydetme biçimleri, sayfa sonları olmayan sürekli bir metin gövdesidir.
// Tüm sayfa sonlarını '\f' karakterleri biçiminde korumak için "ForcePageBreaks" özelliğini "true" olarak ayarlayın.
// Tüm sayfa sonlarını atmak için "ForcePageBreaks" özelliğini "false" olarak ayarlayın.
saveOptions.ForcePageBreaks = forcePageBreaks;

doc.Save(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt", saveOptions);

// Sayfa sonları olan düz metin bir belge yüklersek,
// "Belge" nesnesi bunları gövdeyi sayfalara bölmek için kullanacaktır.
doc = new Document(ArtifactsDir + "TxtSaveOptions.PageBreaks.txt");

Assert.AreEqual(forcePageBreaks ? 3 : 1, doc.PageCount);
```

### Ayrıca bakınız

* class [TxtSaveOptionsBase](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
