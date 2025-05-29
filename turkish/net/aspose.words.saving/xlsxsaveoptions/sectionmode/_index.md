---
title: XlsxSaveOptions.SectionMode
linktitle: SectionMode
articleTitle: SectionMode
second_title: .NET için Aspose.Words
description: XlsxSaveOptions SectionMode özelliğinin XLSX dışa aktarımları için bölüm işlemeyi nasıl optimize ettiğini, sorunsuz belge yönetimini ve birden fazla çalışma sayfasını nasıl sağladığını keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/xlsxsaveoptions/sectionmode/
---
## XlsxSaveOptions.SectionMode property

Bölümlerin çıkış XLSX belgesine kaydedilirken nasıl işleneceğini alır veya ayarlar. Varsayılan değerMultipleWorksheets .

```csharp
public XlsxSectionMode SectionMode { get; set; }
```

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

* enum [XlsxSectionMode](../../xlsxsectionmode/)
* class [XlsxSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
