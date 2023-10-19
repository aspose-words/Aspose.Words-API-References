---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: Aspose.Words for .NET
description: Aspose.Words.Layout.ContinuousSectionRestart Sıralama. Sayfa numaralandırmayı yeniden başlatan sürekli bir bölümde sayfa numaralarını hesaplarken farklı davranışları temsil eder C#'da.
type: docs
weight: 3300
url: /tr/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Sayfa numaralandırmayı yeniden başlatan sürekli bir bölümde sayfa numaralarını hesaplarken farklı davranışları temsil eder.

```csharp
public enum ContinuousSectionRestart
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Always | `0` | Sayfa numaralandırma, içerik akışından bağımsız olarak her zaman yeniden başlar. |
| FromNewPageOnly | `1` | Sayfa numaralandırma, yalnızca bölümün başladığı sayfada bölümden önce başka içerik bulunmadığında yeniden başlar. |

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

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
