---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: .NET için Aspose.Words
description: Belge birleştirmeyi optimize etmek için Aspose.Words.LowCode.MergeFormatMode enum'unu keşfedin. Birden fazla dosyayı zahmetsizce birleştirirken biçimlendirme denetimini geliştirin.
type: docs
weight: 4290
url: /tr/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

Birden fazla belge birleştirildiğinde biçimlendirmenin nasıl birleştirileceğini belirtir.

```csharp
public enum MergeFormatMode
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| MergeFormatting | `0` | Birleştirilen belgelerin biçimlendirmesini birleştirin. |
| KeepSourceFormatting | `1` | Kaynak belgenin, yazı tipi stilleri, boyutlar, renkler, girintiler ve içeriğine uygulanan diğer biçimlendirme öğeleri gibi orijinal biçimlendirmesini koruyacağı anlamına gelir. |
| KeepSourceLayout | `2` | Orijinal belgelerin düzenini son belgede koru. |

## Örnekler

Belgelerin tek bir çıktı belgesinde nasıl birleştirileceğini gösterir.

```csharp
//Belgeleri birleştirmenin birkaç yolu vardır:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* toplantı [Aspose.Words](../../)
