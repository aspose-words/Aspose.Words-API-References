---
title: LayoutOptions.ContinuousSectionPageNumberingRestart
linktitle: ContinuousSectionPageNumberingRestart
articleTitle: ContinuousSectionPageNumberingRestart
second_title: Aspose.Words for .NET
description: LayoutOptions ContinuousSectionPageNumberingRestart mülk. Sürekli bir bölüm sayfa numaralandırmayı yeniden başlattığında sayfa numaralarını hesaplamak için davranış modunu alır veya ayarlar C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.layout/layoutoptions/continuoussectionpagenumberingrestart/
---
## LayoutOptions.ContinuousSectionPageNumberingRestart property

Sürekli bir bölüm sayfa numaralandırmayı yeniden başlattığında sayfa numaralarını hesaplamak için davranış modunu alır veya ayarlar.

```csharp
public ContinuousSectionRestart ContinuousSectionPageNumberingRestart { get; set; }
```

## Notlar

Varsayılan değer:Always. Seçeneğin sunulduğu andaki en son sürüm olan MS Word 2019'un davranışına uygundur. MS Word 2016'nın gösterdiği daha eski sayfa numaralandırma mantığı bu seçenek üzerinden kullanılabilir. Lütfen[`ContinuousSectionRestart`](../../continuoussectionrestart/) davranış açıklaması için.

## Örnekler

Sürekli bir bölümde sayfa numaralandırmanın nasıl kontrol edileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Continuous section page numbering.docx");

// Varsayılan olarak Aspose.Words davranışı Microsoft Word 2019 ile eşleşir.
// Eski Aspose.Words davranışına, tekrarlayan Microsoft Word 2016'ya ihtiyacınız varsa, 'ContinuousSectionRestart.FromNewPageOnly'yi kullanın.
// Sayfa numaralandırma ancak bölümün başladığı sayfada bölümden önce başka içerik kalmadığında yeniden başlar,
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
