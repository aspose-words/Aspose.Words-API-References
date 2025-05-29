---
title: DocumentSplitCriteria Enum
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: .NET için Aspose.Words
description: Aspose.Words.Saving.DocumentSplitCriteria'nın en iyi Html, Epub ve Azw3 formatları için belge bölmeyi nasıl geliştirdiğini keşfedin. Kaydetme sürecinizi kolaylaştırın!
type: docs
weight: 5710
url: /tr/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Belgenin, kaydedilirken parçalara nasıl bölüneceğini belirtirHtml , Epub veyaAzw3 biçim.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belge bölünmedi. |
| PageBreak | `1` | Belge, açık sayfa sonlarıyla parçalara bölünür. Bir sayfa sonu, bir[`PageBreak`](../../aspose.words/controlchar/pagebreak/) karakter, yeni bir sayfada yeni bölümün başlangıcını belirten bir bölüm sonu, veya kendi paragrafı olan bir bölüm sonu[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) özellik ayarlandı`doğru` . |
| ColumnBreak | `2` | Belge, sütun sonlarında parçalara bölünür. Bir sütun sonu, bir[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) or karakteri yeni bir sütunda yeni bölümün başlangıcını belirten bir bölüm sonu. |
| SectionBreak | `4` | Belge herhangi bir türde bölüm sonuyla parçalara bölünür. |
| HeadingParagraph | `8` | Belge, başlık stili kullanılarak biçimlendirilmiş bir paragrafta parçalara bölünür**Başlık 1** ,**Başlık 2** vb. ile birlikte kullanın[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) bölünecek başlık düzeylerini (1'den belirtilen düzeye kadar) belirtmek için |

## Notlar

`DocumentSplitCriteria`birleştirilebilen bir bayrak kümesidir. Örneğin, document 'yi aynı dışa aktarma işleminde sayfa sonlarında ve başlık paragraflarında bölebilirsiniz.

Farklı kriterler kısmen örtüşebilir. Örneğin,**Başlık 1** stile sıklıkla verilir[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) mülk, bu yüzden iki kritere giriyor:PageBreak ve HeadingParagraph. Bazı bölüm sonları sayfa sonlarına vb. neden olabilir. Tipik durumlarda yalnızca bir bayrak belirtmek en pratik seçenektir.

## Örnekler

Bir belgeyi .epub olarak kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydedeceğimiz belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML parçasında olacaktır.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamızı sağlar.
// Belgeyi başlık paragraflarına bölme kriterini belirleyeceğiz.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için yararlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtelim.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
