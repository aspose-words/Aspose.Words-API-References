---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: .NET için Aspose.Words
description: Sürekli bölümlerde kesintisiz sayfa numaralandırma denetimi için LayoutOptions ContinuousSectionPageNumberingRestart özelliğini keşfedin. Belge düzeninizi bugün optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Sürekli bir bölüm sayfa numaralandırmasını yeniden başlattığında sayfa numaralarını hesaplamak için davranış modunu alır veya ayarlar.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Notlar

Varsayılan değer:Always . Bu seçenek, seçeneğin sunulduğu anda en son sürüm olan MS Word 2019'un davranışıyla eşleşir. Bu seçenek aracılığıyla MS Word 2016 tarafından gösterilen daha eski sayfa numaralandırma mantığı kullanılabilir. Lütfen[`ContinuousSectionRestart`](../../continuoussectionrestart/) davranış açıklaması için.

## Örnekler

Sürekli bir bölümde sayfa numaralandırmasının nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Varsayılan olarak Aspose.Words davranışı Microsoft Word 2019 ile eşleşir.
// Eski Aspose.Words davranışına, tekrarlayan Microsoft Word 2016'ya ihtiyacınız varsa, 'ContinuousSectionRestart.FromNewPageOnly' kullanın.
// Sayfa numaralandırması yalnızca bölümün başladığı sayfadaki bölümden önce başka bir içerik yoksa yeniden başlar,
// bu nedenle numaralandırma ikinci sayfadan itibaren 2'ye sıfırlanacaktır.
doc.LayoutOptions.ContinuousSectionPageNumberingRestart = ContinuousSectionRestart.FromNewPageOnly;
doc.UpdatePageLayout();

doc.Save(ArtifactsDir + "Layout.RestartPageNumberingInContinuousSection.pdf");
```

### Ayrıca bakınız

* enum [ContinuousSectionRestart](../../continuoussectionrestart/)
* class [LayoutOptions](../)
* ad alanı [Aspose.Words.Layout](../../../aspose.words.layout/)
* toplantı [Aspose.Words](../../../)
