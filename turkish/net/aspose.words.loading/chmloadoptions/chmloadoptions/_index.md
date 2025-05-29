---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: .NET için Aspose.Words
description: Sorunsuz başlatma için ChmLoadOptions kurucusunu keşfedin. Varsayılan değerleri zahmetsizce ayarlayın ve uygulamanızın performansını bugün artırın!
type: docs
weight: 10
url: /tr/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

Bu sınıfın yeni bir örneğini varsayılan değerlerle başlatır.

```csharp
public ChmLoadOptions()
```

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
