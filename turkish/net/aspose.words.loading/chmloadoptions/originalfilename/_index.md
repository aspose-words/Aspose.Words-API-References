---
title: ChmLoadOptions.OriginalFileName
second_title: Aspose.Words for .NET API Referansı
description: ChmLoadOptions mülk. CHM dosyasının adı. Varsayılan değerhükümsüz .
type: docs
weight: 20
url: /tr/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

CHM dosyasının adı. Varsayılan değer:`hükümsüz` .

```csharp
public string OriginalFileName { get; set; }
```

### Notlar

CHM belgeleri, aynı belgeye dosya adına göre başvuran bağlantılar içerebilir. Aspose.Words bu tür links 'yi destekler ve normalde şunu kullanır:[`OriginalFileName`](../../../aspose.words/document/originalfilename/) link tarafından başvurulan dosyanın yüklenen dosya olup olmadığını kontrol etmek için. Bir belge bir akıştan yükleniyorsa, orijinal dosya adı otomatik olarak belirlenemeyeceği için bu özellik aracılığıyla açıkça belirtilmesi gerekir .

Bir CHM belgesi bir dosyadan yüklenirse ve bu özellik için boş olmayan bir değer belirtilirse, değer, içinde saklanan dosyanın gerçek adına göre önceliğini alacaktır.[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

### Örnekler

"ms-its:myfile.chm::/index.htm" gibi URL'lerin nasıl çözümleneceğini gösterir.

```csharp
// Belgemiz "ms-its:amhelp.chm::....htm" gibi URL'ler içeriyor ancak adı farklı,
// böylece dosya bağlantıları HTML'ye kaydedildikten sonra çalışmaz.
// Bu davranışı önlemek için orijinal dosya adını 'ChmLoadOptions'ta tanımlamamız gerekiyor.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Ayrıca bakınız

* class [ChmLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../chmloadoptions/)
* toplantı [Aspose.Words](../../../)


