---
title: PdfPageLayout Enum
linktitle: PdfPageLayout
articleTitle: PdfPageLayout
second_title: .NET için Aspose.Words
description: En iyi PDF görüntüleme için Aspose.Words.Saving.PdfPageLayout enum'unu keşfedin. Herhangi bir PDF okuyucuda gelişmiş okunabilirlik için sayfa düzenlerini özelleştirin.
type: docs
weight: 6290
url: /tr/net/aspose.words.saving/pdfpagelayout/
---
## PdfPageLayout enumeration

Belge bir PDF okuyucusunda açıldığında kullanılacak sayfa düzenini belirtir.

```csharp
public enum PdfPageLayout
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| SinglePage | `0` | Bir seferde bir sayfa görüntüle. |
| OneColumn | `1` | Sayfaları tek bir sütunda görüntüle. |
| TwoColumnLeft | `2` | Sayfaları iki sütunda, tek numaralı sayfalar solda olacak şekilde görüntüle. |
| TwoColumnRight | `3` | Sayfaları iki sütunda, tek sayılı sayfalar sağda olacak şekilde görüntüle. |
| TwoPageLeft | `4` | Sayfaları ikişer ikişer, tek sayılı sayfaları ise solda görüntüler. |
| TwoPageRight | `5` | Sayfaları ikişer ikişer görüntüle, tek sayılı sayfalar sağda olsun. |

## Örnekler

PDF okuyucusunda açıldığında sayfaların nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Sayfaları ikişer ikişer görüntüle, tek numaralı sayfalar solda olsun.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
