---
title: Enum DocumentSplitCriteria
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Saving.DocumentSplitCriteria Sıralama. Kaydederken belgenin nasıl parçalara bölüneceğini belirtirHtml  Epub veyaAzw3 format.
type: docs
weight: 4960
url: /tr/net/aspose.words.saving/documentsplitcriteria/
---
## DocumentSplitCriteria enumeration

Kaydederken belgenin nasıl parçalara bölüneceğini belirtirHtml , Epub veyaAzw3 format.

```csharp
[Flags]
public enum DocumentSplitCriteria
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| None | `0` | Belge bölünmemiş. |
| PageBreak | `1` | Belge, açık sayfa sonlarıyla parçalara bölünmüştür. Bir sayfa sonu, bir[`PageBreak`](../../aspose.words/controlchar/pagebreak/) karakter, yeni bir sayfada yeni bölümün başlangıcını belirten bölüm sonu, veya kendine ait bir paragraf[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) özellik şu şekilde ayarlandı:`doğru` . |
| ColumnBreak | `2` | Belge, sütun sonlarında parçalara bölünür. Bir sütun sonu, bir[`ColumnBreak`](../../aspose.words/controlchar/columnbreak/) karakter veya yeni bir sütunda yeni bölümün başlangıcını belirten bölüm sonu. |
| SectionBreak | `4` | Belge herhangi bir türdeki bölüm sonunda parçalara bölünür. |
| HeadingParagraph | `8` | Belge, başlık stili kullanılarak biçimlendirilmiş bir paragrafta parçalara bölünmüştür **Başlık 1** , **Başlık 2** vb. Birlikte kullanın[`DocumentSplitHeadingLevel`](../htmlsaveoptions/documentsplitheadinglevel/) bölünecek başlık düzeylerini (1'den belirtilen düzeye kadar) belirtmek için. |

### Notlar

`DocumentSplitCriteria`birleştirilebilen bir dizi bayraktır. Örneğin, aynı dışa aktarma işleminde document 'yi sayfa sonlarında ve başlık paragraflarında bölebilirsiniz.

Farklı kriterler kısmen örtüşebilir. Örneğin, **Başlık 1** stil sıklıkla olarak verilir[`PageBreakBefore`](../../aspose.words/paragraphformat/pagebreakbefore/) özellik, bu nedenle iki kritere girer:PageBreak ve HeadingParagraph. Bazı bölüm sonları sayfa sonlarına vb. neden olabilir. Tipik durumlarda yalnızca bir bayrağın belirtilmesi en pratik seçenektir.

### Örnekler

Bir belgeyi .epub'a kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydedeceğimiz belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML bölümünde bulunur.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamıza olanak tanır.
// Belgeyi başlık paragraflarına bölmek için kriterleri belirleyeceğiz.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için kullanışlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtin.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)


