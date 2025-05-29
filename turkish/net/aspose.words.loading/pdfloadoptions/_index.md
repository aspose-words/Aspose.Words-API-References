---
title: PdfLoadOptions Class
linktitle: PdfLoadOptions
articleTitle: PdfLoadOptions
second_title: .NET için Aspose.Words
description: Gelişmiş PDF yükleme için Aspose.Words.PdfLoadOptions'ı keşfedin. En iyi sonuçlar için esnek seçeneklerle belge dönüşümlerinizi özelleştirin.
type: docs
weight: 4130
url: /tr/net/aspose.words.loading/pdfloadoptions/
---
## PdfLoadOptions class

PDF belgesini bir PDF dosyasına yüklerken ek seçeneklerin belirtilmesine olanak tanır.[`Document`](../../aspose.words/document/) nesne.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yükleme Seçeneklerini Belirleyin](https://docs.aspose.com/words/net/specify-load-options/) belgeleme makalesi.

```csharp
public class PdfLoadOptions : LoadOptions
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PdfLoadOptions](pdfloadoptions/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Gerektiğinde belgede bulunan bağıl URI'leri mutlak URI'lere dönüştürmek için kullanılacak dizeyi alır veya ayarlar. `hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Meta dosyasının dönüştürülüp dönüştürülmeyeceğini alır veya ayarlarWmf veyaEmf ) görüntüleriPnggörüntü biçimi. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Şekillerin EquationXML ile Office Math nesnelerine dönüştürülüp dönüştürülmeyeceğini alır veya ayarlar. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Kodlama belirtilmemişse HTML, TXT veya CHM belgesini yüklemek için kullanılacak kodlamayı alır veya ayarlar belgenin içinde. Şu şekilde olabilir:`hükümsüz` Varsayılan değer:`hükümsüz` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Belge yazı tipi ayarlarının belirlenmesine olanak tanır. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | OLE verilerinin yoksayılıp yoksayılmayacağını belirtir. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Belge yüklenirken kullanılacak dil tercihlerini alır. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Yüklenecek belgenin biçimini belirtir. VarsayılanAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Belge yükleme işleminin belirli bir MS Word sürümüyle eşleşmesi gerektiğini belirtmenize olanak tanır. Varsayılan değerWord2019 |
| [PageCount](../../aspose.words.loading/pdfloadoptions/pagecount/) { get; set; } | Okunacak sayfa sayısını alır veya ayarlar. Varsayılan değer MaxValue'dur, bu da belgenin tüm sayfalarının okunacağı anlamına gelir. |
| [PageIndex](../../aspose.words.loading/pdfloadoptions/pageindex/) { get; set; } | Okunacak ilk sayfanın 0 tabanlı dizinini alır veya ayarlar. Varsayılan 0'dır. |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Şifrelenmiş bir belgeyi açmak için parolayı alır veya ayarlar. Şu şekilde olabilir:`hükümsüz` veya boş dize. Varsayılan`hükümsüz` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Microsoft Word biçimlerini okurken INCLUDEPICTURE alanının korunup korunmayacağını alır veya ayarlar. Varsayılan değer`YANLIŞ` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Bir belge yüklenirken çağrılır ve yükleme ilerlemesiyle ilgili verileri kabul eder. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Bir belge HTML veya MHTML'den içe aktarıldığında harici kaynakların (resimler, stil sayfaları) nasıl yükleneceğini kontrol etmenizi sağlar. |
| [SkipPdfImages](../../aspose.words.loading/pdfloadoptions/skippdfimages/) { get; set; } | PDF belgesi yüklenirken resimlerin atlanması gerekip gerekmediğini belirten bayrağı alır veya ayarlar. Varsayılan:`YANLIŞ` . |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Belgeyi okurken geçici dosyaların kullanılmasına izin verir. Varsayılan olarak bu özellik`hükümsüz` ve geçici dosyalar kullanılmaz. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Alanların güncellenip güncellenmeyeceğini belirtir`kirli` öznitelik. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Sayfa düzeni varsayılan kenar boşluklarını belirlemek için Windows kayıt defterinden alınan LCID değerinin kullanılıp kullanılmayacağını alır veya ayarlar. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Veri veya biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında, yükleme işlemi sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Belirtilen nesnenin geçerli nesneye eşit değerde olup olmadığını belirler. |

## Örnekler

PDF dosyaları yüklenirken resimlerin nasıl atlanacağını gösterir.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### Ayrıca bakınız

* class [LoadOptions](../loadoptions/)
* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
