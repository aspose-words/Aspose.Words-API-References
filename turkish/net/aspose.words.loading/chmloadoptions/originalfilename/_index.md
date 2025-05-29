---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: .NET için Aspose.Words
description: ChmLoadOptions OriginalFileName özelliğini keşfedin, akıcı erişim için CHM dosya adını kolayca ayarlayın. Varsayılan değer null'dır. Deneyiminizi optimize edin!
type: docs
weight: 20
url: /tr/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

CHM dosyasının adı. Varsayılan değer`hükümsüz` .

```csharp
public string OriginalFileName { get; set; }
```

## Notlar

CHM belgeleri, aynı belgeye dosya adıyla başvuran bağlantılar içerebilir. Aspose.Words bu tür bağlantıları destekler ve normalde kullanır[`OriginalFileName`](../../../aspose.words/document/originalfilename/) link tarafından başvurulan dosyanın yüklenen dosya olup olmadığını kontrol etmek için. Bir belge bir akıştan yükleniyorsa, orijinal dosya adı otomatik olarak belirlenemediğinden, bu özellik aracılığıyla açıkça belirtilmelidir.

Bir CHM belgesi bir dosyadan yüklenirse ve bu özellik için boş olmayan bir değer belirtilirse, değer, depolanan dosyanın gerçek adına göre önceliğe sahip olacaktır.[`OriginalFileName`](../../../aspose.words/document/originalfilename/) .

## Örnekler

"ms-its:myfile.chm::/index.htm" gibi URL'lerin nasıl çözüleceğini gösterir.

```csharp
// Belgemiz "ms-its:amhelp.chm::....htm" gibi URL'ler içeriyor, ancak farklı bir adı var,
// dosya HTML'e kaydedildikten sonra bağlantıların çalışmaması.
// Bu davranışı önlemek için 'ChmLoadOptions'da orijinal dosya adını tanımlamamız gerekiyor.
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### Ayrıca bakınız

* class [ChmLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
