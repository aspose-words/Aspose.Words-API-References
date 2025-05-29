---
title: XlsxSectionMode Enum
linktitle: XlsxSectionMode
articleTitle: XlsxSectionMode
second_title: .NET için Aspose.Words
description: Aspose.Words XlsxSectionMode enum'unun XLSX formatında belge kaydetmeyi nasıl optimize ettiğini, iş akışınızı ve belge yönetiminizi nasıl geliştirdiğini keşfedin.
type: docs
weight: 6530
url: /tr/net/aspose.words.saving/xlsxsectionmode/
---
## XlsxSectionMode enumeration

Bir belgeyi XLSX biçiminde kaydederken bölümlerin nasıl işleneceğini belirtir.

```csharp
public enum XlsxSectionMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| MultipleWorksheets | `0` | Bir belgenin her bölümü için ayrı bir çalışma sayfası oluşturulacağını belirtir. |
| SingleWorksheet | `1` | Bir belgenin tüm bölümlerinin tek bir çalışma sayfasına kaydedileceğini belirtir. |

## Örnekler

Belgenin ayrı çalışma sayfaları olarak nasıl kaydedileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Belgenin her bölümü ayrı bir çalışma sayfası olarak oluşturulacak.
// Tüm belgeleri tek bir çalışma sayfasında görüntülemek için 'SingleWorksheet'i kullanın.
XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
xlsxSaveOptions.SectionMode = XlsxSectionMode.MultipleWorksheets;

doc.Save(ArtifactsDir + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
