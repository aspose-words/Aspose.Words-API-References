---
title: ContinuousSectionRestart Enum
linktitle: ContinuousSectionRestart
articleTitle: ContinuousSectionRestart
second_title: .NET için Aspose.Words
description: Sürekli bölümlerde esnek sayfa numaralandırma seçenekleri için Aspose.Words.Layout.ContinuousSectionRestart enumunu keşfedin. Belge düzenini zahmetsizce geliştirin!
type: docs
weight: 3750
url: /tr/net/aspose.words.layout/continuoussectionrestart/
---
## ContinuousSectionRestart enumeration

Sayfa numaralandırmasını yeniden başlatan sürekli bir bölümde sayfa numaralarını hesaplarken farklı davranışları temsil eder.

```csharp
public enum ContinuousSectionRestart
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Always | `0` | İçerik akışından bağımsız olarak sayfa numaralandırma her zaman yeniden başlar. |
| FromNewPageOnly | `1` | Sayfa numaralandırması yalnızca bölümün başladığı sayfadaki bölümden önce başka içerik yoksa yeniden başlar. |

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

* ad alanı [Aspose.Words.Layout](../../aspose.words.layout/)
* toplantı [Aspose.Words](../../)
